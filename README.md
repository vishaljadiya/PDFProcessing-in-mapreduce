# PDFProcessing-in-mapreduce
Processing PDF files in MapReduce
The default inputFormate is TextInputFormate so to process the PDF files we have to customized inputFormate.So in this example we have the class  PDFInputFormate.
Secondly we need similar class like default LineRecorReader so in this example we have PDFReordReader to process PDF files.
Now the main logic is process the PDF files using any library available (I have used PDFBox library )which is used to parse the PDF file to text files. So in this example first we have to parse the PDF files to text files and then process the text files to get the desired requirement.
The RecorReader have Five methods like initialize(),nextKey() etc. 
So in initialize() method We are applying our PDF parsing logic . This method will get the input split and we parses the input split using our pdf parser logic. The output of the pdf parser will be a text which will be stored in a variable. Then we splits the text into multiple lines by using ‘/n’ as the splitter and we will store this lines in  an array.We need to send this as a key-value pair.
Note->There are others PDF parser library available which we can use like Apache Tika etc.We can add the maven dependency accordingly in our pom.xml.
In this example I have disabled the reducer .Just showing hoe to Process the PDF files in MapReduce.
