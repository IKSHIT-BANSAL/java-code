# java-code

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
  
  
