Download Link: https://assignmentchef.com/product/solved-sdev425-week2-fix-your-first-java-data-input-issues
<br>
In this homework you will install Java JDK 8 along with the Netbeans Full IDE bundle. The full bundle provides support for Java, C/C++ and PHP languages. Multiple languages will be used as we detect and mitigate software errors. Becoming comfortable with your programming environment will set the foundation for the rest of the assignments.

If you completed SDEV 325 (which is a prerequisite for this course) you should have already installed the complete Netbeans bundle and essentially the first part of this assignment.

After configuring your environment, you will need to analyze and fix some security issues in a simple Java application that uses a command line argument to enter a filename.

<strong>Assignment </strong>

<h1>Part I: Environment Set-up and Simple Hello, World</h1>

To successfully complete this assignment (and this course), you will need to configure your environment for testing multiple languages. We will use Java JDK and Netbeans to provide this support.

<ol>

 <li>Download and install Java JDK 8 from the Oracle site. Note, you may have previously installed JDK 7 but this course requires JDK 8. The download is available here:</li>

</ol>

<a href="http://www.oracle.com/technetwork/java/javase/downloads/index.html">http://www.oracle.com/technetwork/java/javase/downloads/index.html</a>

You may also need to configure your environment path in Windows. Review the installation guides on the Oracle web sites for details on how to do this.

<ol start="2">

 <li>Download and install Netbeans full IDE. The Full IDE includes Java, Java EE, PHP, C/C++ and server tools. The download is currently available here:</li>

</ol>

https://netbeans.org/downloads/

<ol start="3">

 <li>Once installed, you should review the online documentation and become comfortable starting and running the Netbeans IDE.</li>

 <li>Using Netbeans, create your own unique Hello, World application using the Netbeans IDE for Java. Be sure your code runs properly within the Netbeans environment. Note: part of your unique Hello, World application should include the date and time stamp when the application was run. This should be within your Hello, World code. You can add other unique features as you see fit.</li>

</ol>

<strong> </strong>

<strong>Part II: Fix security issues in a simple Java application that uses command line arguments. </strong>




<ol>

 <li>Download the source file from this week. Found as an attachment in the homework folder.</li>

 <li>Create a new Java application in Netbeans and either copy and paste the code or import the existing source file. Note you may need to make package adjustments if you created a different package</li>

</ol>

Here are text versions of the code and emailaddresses for your reference:

package sdev425;

import java.io.BufferedReader; import java.io.FileReader; import java.io.IOException;




/**

*

<ul>

 <li>@author jim</li>

</ul>

*/

public class SDEV425_1 {




/**

<ul>

 <li>@param args the command line arguments</li>

</ul>

*/

public static void main(String[] args) {

// Read the filename from the command line argument

String filename = args[0];

BufferedReader inputStream = null;




String fileLine;         try {

inputStream = new BufferedReader(new FileReader(filename));

System.out.println(“Email Addresses:”);

// Read one Line using BufferedReader

while ((fileLine = inputStream.readLine()) != null) {

System.out.println(fileLine);

}

} catch (IOException io) {

System.out.println(“File IO exception” + io.getMessage());

} finally {

// Need another catch for closing

// the streams                       try {

if (inputStream != null) {                     inputStream.close();

}

} catch (IOException io) {

System.out.println(“Issue closing the Files” + io.getMessage());

}




}

}




}




EmailAddresses.txt

<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="2f454047416f5a42484c014a4b5a">[email protected]</a> <a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="385e4a5d5c784d555f5b165d5c4d">[email protected]</a> <a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="5e2d2b2d3f301e2b33393d703b3a2b">[email protected]</a> <a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="4a2e2524242b0a3f272d29642f2e3f">[email protected]</a> <a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="523833243b372012273f35317c373627">[email protected]</a> <a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="fe949b8d8d979bbe8b93999dd09b9a8b">[email protected]</a> <a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="fd919c888f9cbd88909a9ed3989988">[email protected]</a> <a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="9de9f4f3fcdde8f0fafeb3f8f9e8">[email protected]</a> <a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="44302b202004312923276a212031">[email protected]</a>

<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="61040521140c06024f040514">[email protected]</a>




<ol start="3">

 <li>Be sure you place the EmailAaddresses.txt file in the Project folder in the root location:</li>

</ol>




<ol start="4">

 <li>You can place the command line argument using the run properties of Netbeans. This screen is invoked by right clicking the project name and the selecting properties. Click on Run and enter the filename. This essentially simulates running java sdev425.SDEV425_1 EmailAddresses.txt at the command line prompt.</li>

</ol>




<ol start="5">

 <li>When you the run the application by clicking the green arrow, you should see output similar to this:</li>

</ol>




Based on the reading and other research you perform, fix any security issues you find in this code