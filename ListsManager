import java.util.*;

public class ListsManager {

    public ArrayList<String> highPriority, lowPriority;  

    public ListsManager() {
      highPriority = new ArrayList<>();
      lowPriority = new ArrayList<>();
    }

    public void addTask(String task) {
      lowPriority.add(task);
    }

    public void removeLowPriorityTask(int index) {
      lowPriority.remove(index);
    }

    public void removeHighPriorityTask(int index) {
      highPriority.remove(index);
    }

    public void changePriority(boolean important, int index) {
      if(important){
        highPriority.add(lowPriority.get(index));
        lowPriority.remove(index);
      }
      else{
        lowPriority.add(0, highPriority.get(index));
        highPriority.remove(index);
      }

    }

    public String toString() {
      String collection = "";
      for(int i=0; i< highPriority.size()-1; i++){
        collection += highPriority.get(i);
      }
      for(int i=0; i< lowPriority.size()-1; i++){
        collection += lowPriority.get(i);
      }
        return collection;  
    }

    public void promote(int index) {
      String temp = highPriority.get(index-1);
      highPriority.set(index-1, highPriority.get(index));
      highPriority.set(index, temp);      
    }
}
