# B4A-iTextGPDF

-----------------
Usage
-----------------

This is just a simple library use for generating pdf files from xHTML strings.
All *.jar, *.xml will go to your additional library folder

IMPORTANT:
This library is intended for educational purpose and non profit use only.

-----------------
Sample Code:
-----------------

	' Basic Html string
	Dim htmlString As StringBuilder
	htmlString.Initialize
	htmlString.append("<html><body> This is HMTL to PDF conversion Example<table border='2' align='center'> ")
	htmlString.append("<tr><td>JavaCodeGeeks</td><td><a href='examples.javacodegeeks.com'>JavaCodeGeeks</a> </td></tr>")		
	htmlString.append("<tr> <td> Google Here </td> <td><a href='www.google.com'>Google</a> </td> </tr></table></body></html>")
	
	' Basic Html File
	Dim pdf As HtmlToPDF
	pdf.convert(htmlString, File.DirRootExternal, "htmltopdf.pdf")				
	
	' Html File with table of items and an embeded image (base64)
	' embeded image like this: <img src="data:image/png;base64....">
	Dim html As String = File.ReadString(File.DirAssets, "invoice.html")
	pdf.convert2(html, File.DirRootExternal, "htmltopdf-invoice.pdf")				
	
	ToastMessageShow("Html2PDF Complete", False)
	
	
	
