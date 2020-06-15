# java-code

package codezen;
import java.util.ArrayList;
import java.util.Date;
import java.util.HashMap;
import java.util.Scanner;
public class abc {
	public static HashMap<Integer, Integer> solution(HashMap<Integer, Integer> map){		
		int key1=-1,key2=-1;
		for(Integer key:map.keySet()) {
			key1=key;
			break;
		}
		for(Integer key:map.keySet()) {
			 key2=key;
		}
		for(int i=key1;i<key2;i++) {
			int v1=map.get(key1);
			int v2=map.get(key2);
			int nextKey=key1+1;
			map.put(nextKey, (v1+v2)/2);
			key1=nextKey;
		}
		return map;
	}

	public static void main(String[] args) {
		HashMap<Integer, Integer> map=new HashMap<Integer, Integer>();
		Scanner s=new Scanner(System.in);
		System.out.println("enter choice 1 to take input 0 to not take input");
		int ch=s.nextInt();
		int key=-1;
		int value=-1;
		
		while(ch!=0) {
			if(ch==1) {
				System.out.println("enter key:");
				 key=s.nextInt();
				System.out.println("enter its value:");
				 value=s.nextInt();
				map.put(key, value);			
			}else {
				System.out.println("do not enter");
			}
			System.out.println("enter choice 1 to take input 0 to not take input");
			ch=s.nextInt();
		}
		solution(map);
	}

}
  
