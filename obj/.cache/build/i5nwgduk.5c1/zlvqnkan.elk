<!DOCTYPE html>
<!--[if IE]><![endif]-->
<html>
  
  <head>
    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1">
    <title>Adapter health </title>
    <meta name="viewport" content="width=device-width">
    <meta name="title" content="Adapter health ">
    <meta name="generator" content="docfx 2.54.0.0">
    
    <link rel="shortcut icon" href="../../../../favicon.ico">
    <link rel="stylesheet" href="../../../../styles/docfx.vendor.css">
    <link rel="stylesheet" href="../../../../styles/docfx.css">
    <link rel="stylesheet" href="../../../../styles/main.css">
    <meta property="docfx:navrel" content="../../../../toc.html">
    <meta property="docfx:tocrel" content="../../../toc.html">
    
    <meta property="docfx:rel" content="../../../../">
    
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
              <a class="navbar-brand" href="../../../../V1/index.html" width="46">
                <img id="logo" src="../../../../V1/main/V1/images/atlas_icon.png" height="46" width="46" alt="OSIsoft Edge System"> 
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
            <article class="content wrap" id="_content" data-uid="AdapterHealth">
<h1 id="adapter-health" sourcefile="V1/main/V1/Health/Adapter health.md" sourcestartlinenumber="5" sourceendlinenumber="5">Adapter health</h1>

<p sourcefile="V1/main/V1/Health/Adapter health.md" sourcestartlinenumber="7" sourceendlinenumber="7">OSIsoft adapters produce different kinds of health data that can be egressed to different health endpoints. </p>
<h2 id="available-health-data" sourcefile="V1/main/V1/Health/Adapter health.md" sourcestartlinenumber="9" sourceendlinenumber="9">Available health data</h2>
<p sourcefile="V1/main/V1/Health/Adapter health.md" sourcestartlinenumber="11" sourceendlinenumber="11">Dynamic data is sent every minute to configured health endpoints.</p>
<p sourcefile="V1/main/V1/Health/Adapter health.md" sourcestartlinenumber="13" sourceendlinenumber="13">The following health data are available:</p>
<ul sourcefile="V1/main/V1/Health/Adapter health.md" sourcestartlinenumber="15" sourceendlinenumber="16">
<li sourcefile="V1/main/V1/Health/Adapter health.md" sourcestartlinenumber="15" sourceendlinenumber="15"><a class="xref" href="Device%20status.html" data-raw-source="[Device status](xref:DeviceStatus)" sourcefile="V1/main/V1/Health/Adapter health.md" sourcestartlinenumber="15" sourceendlinenumber="15">Device status</a></li>
<li sourcefile="V1/main/V1/Health/Adapter health.md" sourcestartlinenumber="16" sourceendlinenumber="16"><a class="xref" href="Next%20health%20message%20expected.html" data-raw-source="[Next Health Message Expected](xref:NextHealthMessageExpected)" sourcefile="V1/main/V1/Health/Adapter health.md" sourcestartlinenumber="16" sourceendlinenumber="16">Next Health Message Expected</a></li>
</ul>
<h2 id="health-endpoint-differences" sourcefile="V1/main/V1/Health/Adapter health.md" sourcestartlinenumber="18" sourceendlinenumber="18">Health endpoint differences</h2>
<p sourcefile="V1/main/V1/Health/Adapter health.md" sourcestartlinenumber="20" sourceendlinenumber="20">Two OMF endpoints are currently supported for adapter health data:</p>
<ul sourcefile="V1/main/V1/Health/Adapter health.md" sourcestartlinenumber="22" sourceendlinenumber="23">
<li sourcefile="V1/main/V1/Health/Adapter health.md" sourcestartlinenumber="22" sourceendlinenumber="22">PI Web API</li>
<li sourcefile="V1/main/V1/Health/Adapter health.md" sourcestartlinenumber="23" sourceendlinenumber="23">OSIsoft Cloud Services</li>
</ul>
<p sourcefile="V1/main/V1/Health/Adapter health.md" sourcestartlinenumber="25" sourceendlinenumber="25">There are a few differences in how these two systems treat the associated health data.</p>
<ul sourcefile="V1/main/V1/Health/Adapter health.md" sourcestartlinenumber="27" sourceendlinenumber="33">
<li sourcefile="V1/main/V1/Health/Adapter health.md" sourcestartlinenumber="27" sourceendlinenumber="31"><p sourcefile="V1/main/V1/Health/Adapter health.md" sourcestartlinenumber="27" sourceendlinenumber="27">PI Web API parses the information and sends it to configured PI servers for the OMF endpoint. The static data is used to create a hierarchy on a PI AF server similar to the following:</p>
<p sourcefile="V1/main/V1/Health/Adapter health.md" sourcestartlinenumber="29" sourceendlinenumber="29"><img src="../images/AdapterHealthAFHierarchy.PNG" alt="AdapterHealthAFHierarchy" sourcefile="V1/main/V1/Health/Adapter health.md" sourcestartlinenumber="29" sourceendlinenumber="29"></p>
<p sourcefile="V1/main/V1/Health/Adapter health.md" sourcestartlinenumber="31" sourceendlinenumber="31">The dynamic health data is time-series data that is stored in PI points on a PI Data Archive. You can see it in the AF hierarchy as PI point data reference attributes.</p>
</li>
<li sourcefile="V1/main/V1/Health/Adapter health.md" sourcestartlinenumber="33" sourceendlinenumber="33"><p sourcefile="V1/main/V1/Health/Adapter health.md" sourcestartlinenumber="33" sourceendlinenumber="33">OSIsoft Cloud Services does not currently provide a way to store the static metadata. For OCS-based adapter health endpoints, only the dynamic data is stored. Each value is its own stream with the timestamp property as the single index.</p>
</li>
</ul>
</article>
          </div>
          
          <div class="hidden-sm col-md-2" role="complementary">
            <div class="sideaffix">
              <div class="contribution">
                <ul class="nav">
                  <li>
                    <a href="https://github.com/osisoft/OSIsoft-Adapter/blob/master/V1/Health/Adapter health.md/#L1" class="contribution-link">Improve this Doc</a>
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
    
    <script type="text/javascript" src="../../../../styles/docfx.vendor.js"></script>
    <script type="text/javascript" src="../../../../styles/docfx.js"></script>
    <script type="text/javascript" src="../../../../styles/main.js"></script>
  </body>
</html>
