---
title: XlsIO Assemblies Required | Syncfusion
description: Briefs the assemblies required for various platforms and frameworks.
platform: File-formats
control: XlsIO
---

# Assemblies Required

The following assemblies need to be referenced in your application based on the platform.
<table>
<tr>
<thead><th>
Platform(s)</th>
<th>
Assembly
</th>
</thead>
</tr>
<tbody>
<tr>
<td>
WPF, Windows Forms, ASP. NET and ASP.NET MVC
</td>
<td>
Syncfusion.XlsIO.Base<br/>
Syncfusion.Compression.Base
</td>
</tr>
<tr>
<td>
Windows Forms and WPF (Client Profile)
</td>
<td>
Syncfusion.XlsIO.ClientProfile<br/>
Syncfusion.Compression.Base
</td>
</tr>
<tr>
<td>
Universal Windows Platform
</td>
<td>
Syncfusion.XlsIO.UWP
</td>
</tr>
<tr>
<td>
.NET Core, Xamarin and Blazor
</td>
<td>
Syncfusion.XlsIO.Portable<br/>
Syncfusion.Compression.Portable
</td>
</tr>
<tr>
<td>
WinRT (Windows Store applications)
</td>
<td>
Syncfusion.XlsIO.WinRT
</td>
</tr>
<tr>
<td>
Windows Phone 8
</td>
<td>
Syncfusion.XlsIO.WP8<br/>
Syncfusion.Compression.WP8
</td>
</tr>
<tr>
<td>
Windows Phone 8.1 Silverlight
</td>
<td>
Syncfusion.XlsIO.WPSilverlight<br/>
Syncfusion.Compression.WPSilverlight
</td>
</tr>
<tr>
<td>
Windows Phone 8.1 WinRT
</td>
<td>
Syncfusion.XlsIO.WP<br/>
Syncfusion.Compression.WP
</td>
</tr>
<tr>
<td>
Silverlight
</td>
<td>
Syncfusion.XlsIO.Silverlight<br/>
Syncfusion.Compression.Silverlight
</td>
</tr>
<tr>
<td>
ASP.NET (Classic)
</td>
<td>
Syncfusion.XlsIO.Web<br/>
Syncfusion.Compression.Base
</td>
</tr>
<tr>
<td>
ASP.NET MVC (Classic)
</td>
<td>
Syncfusion.XlsIO.MVC<br/>
Syncfusion.Compression.Base
</td>
</tr>
<tr>
<td>
Universal (Classic)
</td>
<td>
Syncfusion.XlsIO.Universal
</td>
</tr>
</tbody>
</table>

N> Starting with v16.2.0.x, if you reference Syncfusion assemblies from trial setup or from the NuGet feed, you also have to add "Syncfusion.Licensing" assembly reference and include a license key in your projects. Please refer to this [link](https://help.syncfusion.com/common/essential-studio/licensing/license-key) to know about registering Syncfusion license key in your applications to use our components.

N> Syncfusion components are available in nuget.org

## Converting Excel document to PDF

For converting an Excel document to PDF, the following assemblies need to be referenced in your application.
<table>
<tr>
<th>
Platform(s)
</th>
<th>
Assembly
</th>
</tr>
<tbody>
<tr>
<td>
WPF, Windows Forms, ASP. NET and ASP.NET MVC
</td>
<td>
Syncfusion.XlsIO.Base<br/>
Syncfusion.Compression.Base<br/>
Syncfusion.Pdf.Base<br/>
Syncfusion.ExcelToPDFConverter.Base
</td>
</tr>
<tr>
<td>
Windows Forms and WPF (Client Profile)
</td>
<td>
Syncfusion.XlsIO.ClientProfile<br/>
Syncfusion.Compression.Base<br/>
Syncfusion.Pdf.ClientProfile<br/>
Syncfusion.ExcelToPDFConverter.ClientProfile
</td>
</tr>
<tr>
<td>
UWP, .NET Core, Xamarin and Blazor (Server-Side)
</td>
<td>
Syncfusion.Compression.Portable<br/>
Syncfusion.XlsIO.Portable<br/>
Syncfusion.Pdf.Portable<br/>
Syncfusion.SkiaSharpHelper.Portable<br/>
Syncfusion.XlsIORenderer.Portable
</td>
</tr>
</tbody>
</table>

N> Excel to PDF conversion is supported from .NET Framework 2.0 and .NET Standard 1.4 onwards.

## Converting Excel Worksheet to Image

For converting an Excel worksheet to image, the following assemblies need to be referenced in your application.

<table>
<tr>
<thead><th>
Platform(s)</th>
<th>
Assembly
</th>
</thead>
</tr>
<tbody>
<tr>
<td>
Windows Forms, WPF, ASP.NET and ASP.NET MVC
</td>
<td>
Syncfusion.Compression.Base<br/>
Syncfusion.XlsIO.Base
</td>
</tr>
<tr>
<td>
UWP, .NET Core, Xamarin and Blazor (Server-Side)
</td>
<td>
Syncfusion.Compression.Portable<br/>
Syncfusion.XlsIO.Portable<br/>
Syncfusion.SkiaSharpHelper.Portable<br/>
Syncfusion.XlsIORenderer.Portable
</td>
</tr>
</tbody>
</table>

N> Worksheet to image conversion is supported from .NET Framework 2.0 and .NET Standard 1.4 onwards.

## Converting Excel Chart to Image

For converting an Excel chart to image, the following assemblies need to be referenced in your application.
<table>
<tr>
<th>
Platform(s)
</th>
<th>
Assembly
</th>
</tr>
<tbody>
<tr>
<td>
WPF, Windows Forms, ASP. NET and ASP.NET MVC
</td>
<td>
Syncfusion.Compression.Base<br/>
Syncfusion.XlsIO.Base<br/>
Syncfusion.ExcelChartToImageConverter.WPF<br/>
Syncfusion.SfChart.WPF
</td>
</tr>
<tr>
<td>
UWP, .NET Core, Xamarin and Blazor (Server-Side)
</td>
<td>
Syncfusion.Compression.Portable<br/>
Syncfusion.XlsIO.Portable<br/>
Syncfusion.SkiaSharpHelper.Portable<br/>
Syncfusion.XlsIORenderer.Portable
</td>
</tr>
</tbody>
</table>

N>  Chart to image conversion is supported from .NET Framework 4.0 and .NET Standard 2.0 onwards.

N> Starting with v16.2.0.x, if you reference Syncfusion assemblies from trial setup or from the NuGet feed, you also have to include a license key in your projects. Please refer to this [link](https://help.syncfusion.com/common/essential-studio/licensing/license-key) to know about registering Syncfusion license key in your applications to use our components.
