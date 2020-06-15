# java-code





public class abc {
	public static HashMap<Integer, Integer> solution(HashMap<Integer, Integer> map){	
		
		public static HashMap<Integer, Integer> solution(HashMap<Integer, Integer> map){	
		//map here indicates hashmap like dictionary woth key and values
		//key denotes date in hashmap
		
		
		int key1=-1,key2=-1;
		for(Integer key:map.keySet()) {
			key1=key;
			break;
		}
		for(Integer key:map.keySet()) {
			 key2=key;
		}
		//keys are fetched which are taken here
		for(int i=key1;i<key2;i++) {
			int v1=map.get(key1);
			int v2=map.get(key2);
			int nextKey=key1+1;
			map.put(nextKey, (v1+v2)/2);
			key1=nextKey;
		}
		//map is return as required for the answer.
		return map;
	}
  }



UNIT TESTS

dictionary given

input={2017-03-04:100 , 2017-03-07:115}

output={2017-03-04:100 , 2017-03-05:105 , 2017-03-06:110 , 2017-03-07:115}
