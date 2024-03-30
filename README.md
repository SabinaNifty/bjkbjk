# TestingProgram
My Git repo with Eclipse Java
import com.google.gson.Gson;

class RepositoryStatistics {
 String location;
 StatOfRepository stat_of_repository;
 StatOfWarnings stat_of_warnings;

 RepositoryStatistics(String location, StatOfRepository stat_of_repository, StatOfWarnings stat_of_warnings) {
     this.location = location;
     this.stat_of_repository = stat_of_repository;
     this.stat_of_warnings = stat_of_warnings;
 }
}

class StatOfRepository {
 int number_of_commits;
 double avg_of_num_java_files;
 double avg_of_num_warnings;

 StatOfRepository(int number_of_commits, double avg_of_num_java_files, double avg_of_num_warnings) {
     this.number_of_commits = number_of_commits;
     this.avg_of_num_java_files = avg_of_num_java_files;
     this.avg_of_num_warnings = avg_of_num_warnings;
 }
}

class StatOfWarnings {
 int AbstractClassWithoutAbstractMethod;
 int AvoidReassigningCatchVariables;
 // Add other warning types as needed

 StatOfWarnings(int abstractClassWithoutAbstractMethod, int avoidReassigningCatchVariables) {
     this.AbstractClassWithoutAbstractMethod = abstractClassWithoutAbstractMethod;
     this.AvoidReassigningCatchVariables = avoidReassigningCatchVariables;
     // Initialize other warning types
 }
}

public class Master {
 public static void main(String[] args) {
     // Create sample data
     StatOfRepository repositoryStats = new StatOfRepository(101, 30.2, 193.2);
     StatOfWarnings warningStats = new StatOfWarnings(1908, 2020);
     // Add more warning types if needed

     RepositoryStatistics stats = new RepositoryStatistics("/a/b/c", repositoryStats, warningStats);

     // Convert Java object to JSON string
     Gson gson = new Gson();
     String json = gson.toJson(stats);

     // Print JSON string with formatted layout
     System.out.println("{");
     System.out.println("	“location”: “" + stats.location + "”,");
     System.out.println("	“stat_of_repository”:  " );
     System.out.println("        { " );

     System.out.println("    		“number_of_commits”: " + stats.stat_of_repository.number_of_commits +",");
     System.out.println("   		“avg_of_num_java_files”: " + stats.stat_of_repository.avg_of_num_java_files + ",");
     System.out.println("   	        “avg_of_num_warnings”: " + stats.stat_of_repository.avg_of_num_warnings + ",");
     System.out.println(" 	 }");
     System.out.println("         “stat_of_warnings”: ");
     System.out.println("                 {");

     System.out.println("   		         “AbstractClassWithoutAbstractMethod”: " + stats.stat_of_warnings.AbstractClassWithoutAbstractMethod + ",");
     System.out.println("   		         “AvoidReassigningCatchVariables”: " + stats.stat_of_warnings.AvoidReassigningCatchVariables + ",");
     System.out.println("                          ...");
     System.out.println("                  }");
     System.out.println("}");
 }
}

