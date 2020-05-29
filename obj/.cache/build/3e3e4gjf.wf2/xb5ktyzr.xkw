<!DOCTYPE html>
<!--[if IE]><![endif]-->
<html>
  
  <head>
    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1">
    <title>OSIsoft Adapter for Modbus TCP supported features </title>
    <meta name="viewport" content="width=device-width">
    <meta name="title" content="OSIsoft Adapter for Modbus TCP supported features ">
    <meta name="generator" content="docfx 2.54.0.0">
    
    <link rel="shortcut icon" href="../../favicon.ico">
    <link rel="stylesheet" href="../../styles/docfx.vendor.css">
    <link rel="stylesheet" href="../../styles/docfx.css">
    <link rel="stylesheet" href="../../styles/main.css">
    <meta property="docfx:navrel" content="../../toc.html">
    <meta property="docfx:tocrel" content="../toc.html">
    
    <meta property="docfx:rel" content="../../">
    
  </head>
  <body data-spy="scroll" data-target="#affix" data-offset="120">
    <div id="wrapper">
      <header>
        
        <nav id="autocollapse" class="navbar navbar-inverse ng-scope" role="navigation">
          <div class="container">
            <div class="navbar-header">
              <button type="button" class="navbar-toggle" data-toggle="collapse" data-target="#navbar">
                <span class="sr-only">Toggle navigation</span>
                <span class="icon-bar"></span>
                <span class="icon-bar"></span>
                <span class="icon-bar"></span>
              </button>
              <a class="navbar-brand" href="../../V1/index.html" width="46">
                <img id="logo" src="../../V1/main/V1/images/atlas_icon.png" height="46" width="46" alt="OSIsoft Edge System"> 
              </a>
            </div>
            <div class="collapse navbar-collapse" id="navbar">
              <form class="navbar-form navbar-right" role="search" id="search">
                <div class="form-group">
                  <input type="text" class="form-control" id="search-query" placeholder="Search" autocomplete="off">
                </div>
              </form>
            </div>
          </div>
        </nav>
        
        <div class="subnav navbar navbar-default">
          <div class="container hide-when-search" id="breadcrumb">
            <ul class="breadcrumb">
              <li></li>
            </ul>
          </div>
        </div>
      </header>
      <div class="container body-content">
        
        <div id="search-results">
          <div class="search-list"></div>
          <div class="sr-items">
            <p><i class="glyphicon glyphicon-refresh index-loading"></i></p>
          </div>
          <ul id="pagination"></ul>
        </div>
      </div>
      <div role="main" class="container body-content hide-when-search">
        
        <div class="sidenav hide-when-search">
          <a class="btn toc-toggle collapse" data-toggle="collapse" href="#sidetoggle" aria-expanded="false" aria-controls="sidetoggle">Show / Hide Table of Contents</a>
          <div class="sidetoggle collapse" id="sidetoggle">
            <div id="sidetoc"></div>
          </div>
        </div>
        <div class="article row grid-right">
          <div class="col-md-10">
            <article class="content wrap" id="_content" data-uid="OSIsoftAdapterForModbusTCPSupportedFeatures">
<h1 id="osisoft-adapter-for-modbus-tcp-supported-features" sourcefile="V1/OSIsoft Adapter for Modbus TCP overview/OSIsoft Adapter for Modbus TCP supported features.md" sourcestartlinenumber="5" sourceendlinenumber="5">OSIsoft Adapter for Modbus TCP supported features</h1>

<p sourcefile="V1/OSIsoft Adapter for Modbus TCP overview/OSIsoft Adapter for Modbus TCP supported features.md" sourcestartlinenumber="7" sourceendlinenumber="7">For certain data types, the adapter supports applying bitmaps and applying data conversion.</p>
<h2 id="bitmap-application" sourcefile="V1/OSIsoft Adapter for Modbus TCP overview/OSIsoft Adapter for Modbus TCP supported features.md" sourcestartlinenumber="9" sourceendlinenumber="9">Bitmap application</h2>
<p sourcefile="V1/OSIsoft Adapter for Modbus TCP overview/OSIsoft Adapter for Modbus TCP supported features.md" sourcestartlinenumber="11" sourceendlinenumber="11">The adapter supports applying bitmaps to the value converted from reading the Modbus TCP devices. A bitmap is a series of numbers used to extract and reorder bits from a word register. The format of the bitmap is <code>uuvvwwxxyyzz</code>, where <code>uu</code>, <code>vv</code>, <code>ww</code>, <code>yy</code>, and <code>zz</code> each refer to a single bit. Bitmaps require a leading zero if the referenced bit is less than 10. The low-order bit is 01 and high-order bit is either 16 or 32. Bitmaps can reference up to 16 bits for a 16-bit word (data types 10 and 20) and up to 32 bits for a 32-bit word (data type 30 and 31).</p>
<p sourcefile="V1/OSIsoft Adapter for Modbus TCP overview/OSIsoft Adapter for Modbus TCP supported features.md" sourcestartlinenumber="13" sourceendlinenumber="13">For example, the bitmap <code>0307120802</code> maps the second bit of the original word to the first bit of the new word, the eighth bit to the second bit, the twelfth bit to the third bit, and so on. The high-order bits of the new word are padded with zeros if they are not specified.</p>
<p sourcefile="V1/OSIsoft Adapter for Modbus TCP overview/OSIsoft Adapter for Modbus TCP supported features.md" sourcestartlinenumber="15" sourceendlinenumber="15">Not all data types support bitmapping. The data types that support bitmaps include:</p>
<ul sourcefile="V1/OSIsoft Adapter for Modbus TCP overview/OSIsoft Adapter for Modbus TCP supported features.md" sourcestartlinenumber="17" sourceendlinenumber="19">
<li sourcefile="V1/OSIsoft Adapter for Modbus TCP overview/OSIsoft Adapter for Modbus TCP supported features.md" sourcestartlinenumber="17" sourceendlinenumber="17"><code>Int16</code> (Data type code <code>10</code>)</li>
<li sourcefile="V1/OSIsoft Adapter for Modbus TCP overview/OSIsoft Adapter for Modbus TCP supported features.md" sourcestartlinenumber="18" sourceendlinenumber="18"><code>UInt16</code> (Data type code <code>20</code>)</li>
<li sourcefile="V1/OSIsoft Adapter for Modbus TCP overview/OSIsoft Adapter for Modbus TCP supported features.md" sourcestartlinenumber="19" sourceendlinenumber="19"><code>Int32</code> (Data type code <code>30</code> and <code>31</code>)</li>
</ul>
<h2 id="data-conversion-application" sourcefile="V1/OSIsoft Adapter for Modbus TCP overview/OSIsoft Adapter for Modbus TCP supported features.md" sourcestartlinenumber="21" sourceendlinenumber="21">Data conversion application</h2>
<p sourcefile="V1/OSIsoft Adapter for Modbus TCP overview/OSIsoft Adapter for Modbus TCP supported features.md" sourcestartlinenumber="23" sourceendlinenumber="23">The adapter supports applying data conversion to the value converted from reading Modbus TCP devices. You can specify a conversion factor and conversion offset. The conversion factor is used for scaling the value up or down and the conversion offset is used for shifting the value. The mathematical equation for conversion is represented below:</p>
<pre sourcefile="V1/OSIsoft Adapter for Modbus TCP overview/OSIsoft Adapter for Modbus TCP supported features.md" sourcestartlinenumber="25" sourceendlinenumber="27"><code class="lang-code">&lt;After Conversion&gt; = &lt;Before Conversion&gt; / Factor - Offset
</code></pre><p sourcefile="V1/OSIsoft Adapter for Modbus TCP overview/OSIsoft Adapter for Modbus TCP supported features.md" sourcestartlinenumber="29" sourceendlinenumber="29"> Not all data types support applying data conversion. Data types that support data conversion include:</p>
<ul sourcefile="V1/OSIsoft Adapter for Modbus TCP overview/OSIsoft Adapter for Modbus TCP supported features.md" sourcestartlinenumber="31" sourceendlinenumber="34">
<li sourcefile="V1/OSIsoft Adapter for Modbus TCP overview/OSIsoft Adapter for Modbus TCP supported features.md" sourcestartlinenumber="31" sourceendlinenumber="31"><code>Int16</code> (Data type code <code>10</code>)</li>
<li sourcefile="V1/OSIsoft Adapter for Modbus TCP overview/OSIsoft Adapter for Modbus TCP supported features.md" sourcestartlinenumber="32" sourceendlinenumber="32"><code>UInt16</code> (Data type code <code>20</code>)</li>
<li sourcefile="V1/OSIsoft Adapter for Modbus TCP overview/OSIsoft Adapter for Modbus TCP supported features.md" sourcestartlinenumber="33" sourceendlinenumber="33"><code>Int32</code> (Data type code <code>30</code> and <code>31</code>)</li>
<li sourcefile="V1/OSIsoft Adapter for Modbus TCP overview/OSIsoft Adapter for Modbus TCP supported features.md" sourcestartlinenumber="34" sourceendlinenumber="34"><code>Float32</code> (Data type code <code>100</code> and <code>101</code>)</li>
</ul>
<p sourcefile="V1/OSIsoft Adapter for Modbus TCP overview/OSIsoft Adapter for Modbus TCP supported features.md" sourcestartlinenumber="36" sourceendlinenumber="36">The value with data conversion applied is always converted to the 32-bit float type to maintain the precision of the conversion factor and conversion offset.</p>
</article>
          </div>
          
          <div class="hidden-sm col-md-2" role="complementary">
            <div class="sideaffix">
              <div class="contribution">
                <ul class="nav">
                  <li>
                    <a href="https://github.com/osisoft/OSIsoft-Adapter-Modbus-Docs/blob/master/V1/OSIsoft Adapter for Modbus TCP overview/OSIsoft Adapter for Modbus TCP supported features.md/#L1" class="contribution-link">Improve this Doc</a>
                  </li>
                </ul>
              </div>
              <nav class="bs-docs-sidebar hidden-print hidden-xs hidden-sm affix" id="affix">
              <!-- <p><a class="back-to-top" href="#top">Back to top</a><p> -->
              </nav>
            </div>
          </div>
        </div>
      </div>
      
      <footer>
        <div class="grad-bottom"></div>
        <div class="footer">
          <div class="container">
            <span class="pull-right">
              <a href="#top">Back to top</a>
            </span>
            
            <span>© 2020 - OSIsoft, LLC.</span>
          </div>
        </div>
      </footer>
    </div>
    
    <script type="text/javascript" src="../../styles/docfx.vendor.js"></script>
    <script type="text/javascript" src="../../styles/docfx.js"></script>
    <script type="text/javascript" src="../../styles/main.js"></script>
  </body>
</html>
