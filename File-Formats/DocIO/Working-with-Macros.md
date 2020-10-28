---
title: Working with Macros | DocIO | Syncfusion
description: This section illustrates how to load and save a macro enabled documents
platform: file-formats
control: DocIO
documentation: UG
---
# Working with Macros

Macro is a way to automate the tasks that you perform repeatedly. It is a saved sequence of commands or keyboard strokes that can be recalled with a single command or keyboard stroke. 

The following link shows how to create a macro in the Word document.

[https://support.office.com/en-in/article/Create-or-run-a-macro-c6b99036-905c-49a6-818a-dfb98b7c3c9c](https://support.office.com/en-in/article/Create-or-run-a-macro-c6b99036-905c-49a6-818a-dfb98b7c3c9c#)

The following code illustrates how to load and save a macro enabled document.

{% tabs %}  

{% highlight c# %}

//Loads the macro-enabled template
WordDocument document = new WordDocument("Template.dotm");
//Gets the table
DataTable table = GetDataTable();
//Executes Mail Merge with groups
document.MailMerge.ExecuteGroup(table);
//Saves and closes the document
document.Save("Sample.docm", FormatType.Word2013Docm);
document.Close();

{% endhighlight %}

{% highlight vb.net %}

'Loads the macro-enabled template
Dim document As New WordDocument("Template.dotm")
'Gets the table
Dim table As DataTable = GetDataTable()
'Executes Mail Merge with groups
document.MailMerge.ExecuteGroup(table)
'Saves and closes the document
document.Save("Sample.docm", FormatType.Word2013Docm)
document.Close()

{% endhighlight %}

{% highlight UWP %}
//DocIO supports mail merge operation in Windows Forms, WPF, ASP.NET and ASP.NET MVC platforms alone.
{% endhighlight %}

{% highlight ASP.NET CORE %}
//DocIO supports mail merge operation in Windows Forms, WPF, ASP.NET and ASP.NET MVC platforms alone.
{% endhighlight %}

{% highlight XAMARIN %}
//DocIO supports mail merge operation in Windows Forms, WPF, ASP.NET and ASP.NET MVC platforms alone.
{% endhighlight %}

{% endtabs %}  

The following code example illustrates the method used to get the tables from data set.

{% tabs %}  

{% highlight c# %}

private DataTable GetDataTable()
{
	//List of syncfusion products name
	string[] products = { "DocIO", "PDF", "XlsIO" };
	//Adds new Tables to the data set
	DataRow row;
	DataTable table = new DataTable();
	//Adds fields to the Products table
	table.TableName = "Products";
	table.Columns.Add("ProductName");
	table.Columns.Add("Binary");
	table.Columns.Add("Source");
	//Inserts values to the tables
	foreach (string product in products)
	{
		row = table.NewRow();
		row["ProductName"] = string.Concat("Essential ", product);
		row["Binary"] = "$895.00";
		row["Source"] = "$1,295.00";
		table.Rows.Add(row);
	}
	return table;
}

{% endhighlight %}

{% highlight vb.net %}

Private Function GetDataTable() As DataTable
	'List of syncfusion products name
	Dim products As String() = {"DocIO", "PDF", "XlsIO"}
	'Adds new Tables to the data set
	Dim row As DataRow
	Dim table As New DataTable()
	'Adds fields to the Products table
	table.TableName = "Products"
	table.Columns.Add("ProductName")
	table.Columns.Add("Binary")
	table.Columns.Add("Source")
	'Inserts values to the tables
	For Each product As String In products
		row = table.NewRow()
		row("ProductName") = String.Concat("Essential ", product)
		row("Binary") = "$895.00"
		row("Source") = "$1,295.00"
		table.Rows.Add(row)
	Next
	Return table
End Function 

{% endhighlight %}

{% highlight UWP %}
//DocIO supports mail merge operation in Windows Forms, WPF, ASP.NET and ASP.NET MVC platforms alone.
{% endhighlight %}

{% highlight ASP.NET CORE %}
//DocIO supports mail merge operation in Windows Forms, WPF, ASP.NET and ASP.NET MVC platforms alone.
{% endhighlight %}

{% highlight XAMARIN %}
//DocIO supports mail merge operation in Windows Forms, WPF, ASP.NET and ASP.NET MVC platforms alone.
{% endhighlight %} 

{% endtabs %} 

The following code example illustrates how to remove the macros present in the document by using `RemoveMacros` method.

{% tabs %}  

{% highlight c# %}

//Loads the document with macros
WordDocument document = new WordDocument("Sample.docm");
//Checks whether the document has macros and then removes them
if (document.HasMacros)
	document.RemoveMacros();
//Saves the document
document.Save("Sample.docx", FormatType.Docx);
//Closes the document
document.Close();

{% endhighlight %}

{% highlight vb.net %}

'Loads the document with macros
Dim document As New WordDocument("Sample.docm")
'Checks whether the document has macros and then removes them
If document.HasMacros Then
	document.RemoveMacros()
End If
'Saves the document
document.Save("Sample.docx", FormatType.Docx)
'Closes the document
document.Close()

{% endhighlight %}

{% highlight UWP %}
//Loads the document with macros
Assembly assembly = typeof(App).GetTypeInfo().Assembly;
WordDocument document = new WordDocument(assembly.GetManifestResourceStream("Sample.Assets.Sample.docm"), FormatType.Docx);
//Checks whether the document has macros and then removes them
if (document.HasMacros)
	document.RemoveMacros();
//Saves the Word file to MemoryStream
MemoryStream stream = new MemoryStream();
await document.SaveAsync(stream, FormatType.Docx);
//Saves the stream as Word file in local machine
Save(stream, "Sample.docx");
//Closes the document
document.Close();
//Please refer the below link to save Word document in UWP platform
//https://help.syncfusion.com/file-formats/docio/create-word-document-in-uwp#save-word-document-in-uwp
{% endhighlight %}

{% highlight ASP.NET CORE %}
//Loads the document with macros
FileStream fileStreamPath = new FileStream("Sample.docm", FileMode.Open, FileAccess.Read, FileShare.ReadWrite);
WordDocument document = new WordDocument(fileStreamPath, FormatType.Docx);
//Checks whether the document has macros and then removes them
if (document.HasMacros)
	document.RemoveMacros();
//Saves the Word document to MemoryStream
MemoryStream stream = new MemoryStream();
document.Save(stream, FormatType.Docx);
//Closes the document
document.Close();
stream.Position = 0;
//Download Word document in the browser
return File(stream, "application/msword", "Sample.docx");
{% endhighlight %}

{% highlight XAMARIN %}
//Loads the document with macros
Assembly assembly = typeof(App).GetTypeInfo().Assembly;
WordDocument document = new WordDocument(assembly.GetManifestResourceStream("GettingStarted.Data.Sample.docm"), FormatType.Docx);
//Checks whether the document has macros and then removes them
if (document.HasMacros)
	document.RemoveMacros();
//Saves the Word document to  MemoryStream
MemoryStream stream = new MemoryStream();
document.Save(stream, FormatType.Docx);
//Closes the document
document.Close();
//Save the stream as a file in the device and invoke it for viewing
Xamarin.Forms.DependencyService.Get<ISave>().SaveAndView("Sample.docx", "application/msword", stream);
//Please download the helper files from the below link to save the stream as file and open the file for viewing in Xamarin platform
//https://help.syncfusion.com/file-formats/docio/create-word-document-in-xamarin#helper-files-for-xamarin
{% endhighlight %}

{% endtabs %}  