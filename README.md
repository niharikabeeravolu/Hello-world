# Hello-world
just another repository
 
 As a second step let us add Jersey Framework and its dependencies (libraries) in our project. Copy all jars from following directories of download jersey zip folder in WEB-INF/lib directory of the project.
 
 The first step is to create a Dynamic Web Project using Eclipse IDE. Follow the option File -> New -> Project and finally select Dynamic Web Project wizard from the wizard list. Now name your project as UserManagement using the wizard window as follows:
 v
 The first step is to create a Dynamic Web Project using Eclipse IDE. Follow the option File -> New -> Project and finally select Dynamic Web Project wizard from the wizard list. Now name your project as UserManagement using the wizard window as follows:

ackage com.tutorialspoint;

import java.io.Serializable;

import javax.xml.bind.annotation.XmlElement;
import javax.xml.bind.annotation.XmlRootElement;
@XmlRootElement(name = "user")
public class User implements Serializable {

   private static final long serialVersionUID = 1L;
   private int id;
   private String name;
   private String profession;

   public User(){}
   
   public User(int id, String name, String profession){
      this.id = id;
      this.name = name;
      this.profession = profession;
   }

   public int getId() {
      return id;
   }

   @XmlElement
   public void setId(int id) {
      this.id = id;
   }
   public String getName() {
      return name;
   }
   @XmlElement
   public void setName(String name) {
      this.name = name;
   }
   public String getProfession() {
      return profession;
   }
   @XmlElement
   public void setProfession(String profession) {
      this.profession = profession;
   }		
}
