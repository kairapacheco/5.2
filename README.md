public class Task extends taskDriver implements Priority, Comparable
{
   private String task, assignment;
   private int priorityLevel;
   
   public Task (String assignment)
   {
      task = assignment;
      priorityLevel = 0;
   }//assigns different variables
   
   public void setPriority (int level)
   {
      priorityLevel = level;
   }//sets the priorityLevel
   
   public int getPriority()
   {
      return priorityLevel;
   }//return the priorityLevel
   
   public int compareTo(Object obj)
   {
    int otherPriorityLevel = ((Task)obj).getPriority();
    int result; 
    if (priorityLevel < otherPriorityLevel)
        {
        //System.out.println("First");
        result = -1;
    }
    else if (priorityLevel > otherPriorityLevel)
    {
        //System.out.println("Second");
        result = 0;
    }
    else 
    {
        //System.out.println("Third");
        result = 1;
    }
        return result;
   }//end of method compareTo
    
   public String toString()
   {
      return task + "";
   }//end of toString
   
}//end of class Question implements Complexity, Comparable
