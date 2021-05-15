import java.util.sql.*;
public class DBconnection
{
    Connection con;
    DBconnection()
    {
        try
        {
            class.ForName("com.mysql.jdbc.Driver");
            String connectionURL="jdbc:mysql://localhost:3306/Practical";
            String dbuser="root";
            String dbpass="lakhmani";
            con=DriverManager.getConnection(connectionURL,dbuser,dbpass);
            System.out.println("Connection Successfull");
        }
        catch(Exception e)
        {
            System.out.println("Connection Failed" + e);
        }
        public static void main(String args[])
        {
            DBconnection obj = new DBconnection();
        }

    }
    import java.sql.*;
    import java.util.Scanner;
    public class operation extends DBconnection
    {
        void insert()
        {
            try
            {
                Scanner sc = new Scanner(System.in);
                System.out.println("Enter Student Id");
                int id = sc.nextInt();
                System.out.println("Enter student name");
                String name= sc.next();
                System.out.println("Enter student mobile number");
                int mobile = sc.nextInt();
                System.out.println("Enter Student email");
                String email= sc.next();

                String insertquery = "insert into student values(?,?,?,?)"
                        PreparedStatement pst = con.prepareStatement(insertquery);
                pst.setInt(1,id);
                pst.setString(2,name);
                pst.setInt(3,mobile);
                pst.setString(4,email);
                pst.executeUpdate();

                System.out.println("data inserted");

            }
            catch(Exception e)
            {
                System.out.println("Data not inserted" + e);
            }
        }
        void Delete()
        {
            try
            {
                Scanner sc = new Scanner(System.in);
                int id = sc.nextInt();
                String delquery= "delete from student id = " + id;
                PreparedStatement pst = con.prepareStatement(delquery);
                pst.executeUpdate();
                System.out.println("Data deleted");
            }
            catch(Exception e)
            {
                System.out.println("Data not deleted" + e);
            }
        }
        void view()
        {
            try
            {
             String viewquery= "select * from student where id ="01"";
             Statement St = con.CreateStatement();
             ResultSet rs = St.executeQuery(viewquery);
             while(rs.next())
             {
                 System.out.println(" " + rs.getInt(1));
                 System.out.println(" " + rs.getstring(2));
                 System.out.println(" " + rs.getInt(3));
                 System.out.println(" " + rs.getString(4));
             }
            }
            catch (Exception e)
            {
                System.out.println("Data not found" + e);
            }
        }
        void update()
        {
            try
            {
                String name = "navin";
                String updatequery="Update Student set sname=" " + name + "" ";
                PrepareStatement pst = con.preparestatement(Updatequery);
                pst.executeupdate();
                System.out.println("update sucessfull");
            }
            catch(Exception e)
            {
                Systm.out.println("Update not sucessfull" + e);
            }
        }
        public static void main(string args[])
        {
            operation obj = new operation();
        }
    }
}
