<!DOCTYPE html>
<!--[if IE]><![endif]-->
<html>
  
  <head>
    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1">
    <title>Diagnostics configuration </title>
    <meta name="viewport" content="width=device-width">
    <meta name="title" content="Diagnostics configuration ">
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
            <article class="content wrap" id="_content" data-uid="DiagnosticsConfiguration">
<h1 id="diagnostics-configuration" sourcefile="V1/main/V1/ARCHIVE/Diagnostics configuration.md" sourcestartlinenumber="5" sourceendlinenumber="5">Diagnostics configuration</h1>

<p sourcefile="V1/main/V1/ARCHIVE/Diagnostics configuration.md" sourcestartlinenumber="7" sourceendlinenumber="8">You can configure OSIsoft adapters to produce and store diagnostics data at a designated health endpoint.
For more information about available diagnostics data, see <a class="xref" href="../Diagnostics/Adapter%20diagnostics.html" data-raw-source="[Adapter diagnostics](xref:AdapterDiagnostics)" sourcefile="V1/main/V1/ARCHIVE/Diagnostics configuration.md" sourcestartlinenumber="8" sourceendlinenumber="8">Adapter diagnostics</a>.</p>
<h2 id="configure-diagnostics" sourcefile="V1/main/V1/ARCHIVE/Diagnostics configuration.md" sourcestartlinenumber="10" sourceendlinenumber="10">Configure diagnostics</h2>
<ol sourcefile="V1/main/V1/ARCHIVE/Diagnostics configuration.md" sourcestartlinenumber="12" sourceendlinenumber="21">
<li sourcefile="V1/main/V1/ARCHIVE/Diagnostics configuration.md" sourcestartlinenumber="12" sourceendlinenumber="12">Start any of the <a class="xref" href="../Configuration/Configuration%20tools.html" data-raw-source="[Configuration tools](xref:ConfigurationTools)" sourcefile="V1/main/V1/ARCHIVE/Diagnostics configuration.md" sourcestartlinenumber="12" sourceendlinenumber="12">Configuration tools</a> capable of making HTTP requests.</li>
<li sourcefile="V1/main/V1/ARCHIVE/Diagnostics configuration.md" sourcestartlinenumber="13" sourceendlinenumber="21"><p sourcefile="V1/main/V1/ARCHIVE/Diagnostics configuration.md" sourcestartlinenumber="13" sourceendlinenumber="13">Run a <code>PUT</code> command to the following endpoint and set the <code>enableDiagnostics</code> parameter to either <strong>true</strong> or <strong>false</strong>: <code>http://localhost:5590/api/v1/configuration/system/diagnostics</code></p>
<p sourcefile="V1/main/V1/ARCHIVE/Diagnostics configuration.md" sourcestartlinenumber="15" sourceendlinenumber="15"><strong>Note:</strong> <code>5590</code> is the default port number. If you selected a different port number, replace it with that value.</p>
<p sourcefile="V1/main/V1/ARCHIVE/Diagnostics configuration.md" sourcestartlinenumber="17" sourceendlinenumber="17">Example using <code>curl</code>:</p>
<pre sourcefile="V1/main/V1/ARCHIVE/Diagnostics configuration.md" sourcestartlinenumber="19" sourceendlinenumber="21"><code class="lang-bash">curl -d &quot;{ &quot;enableDiagnostics&quot;:true }&quot; -X PUT &quot;http://localhost:5590/api/v1/configuration/system/diagnostics&quot;
</code></pre></li>
</ol>
<h2 id="diagnostics-schema" sourcefile="V1/main/V1/ARCHIVE/Diagnostics configuration.md" sourcestartlinenumber="23" sourceendlinenumber="23">Diagnostics schema</h2>
<p sourcefile="V1/main/V1/ARCHIVE/Diagnostics configuration.md" sourcestartlinenumber="25" sourceendlinenumber="25">The full schema definition for the diagnostics configuration is in the <em>System_Diagnostics_schema.json</em> here:</p>
<p sourcefile="V1/main/V1/ARCHIVE/Diagnostics configuration.md" sourcestartlinenumber="27" sourceendlinenumber="27">Windows: <em>%ProgramFiles%\OSIsoft\Adapters\AdapterName\Schemas</em></p>
<p sourcefile="V1/main/V1/ARCHIVE/Diagnostics configuration.md" sourcestartlinenumber="29" sourceendlinenumber="29">Linux: <em>/opt/OSIsoft/Adapters/AdapterName/Schemas</em></p>
<h2 id="diagnostics-parameters" sourcefile="V1/main/V1/ARCHIVE/Diagnostics configuration.md" sourcestartlinenumber="31" sourceendlinenumber="31">Diagnostics parameters</h2>
<p sourcefile="V1/main/V1/ARCHIVE/Diagnostics configuration.md" sourcestartlinenumber="33" sourceendlinenumber="33">The following parameters are available for configuring diagnostics:</p>
<table sourcefile="V1/main/V1/ARCHIVE/Diagnostics configuration.md" sourcestartlinenumber="35" sourceendlinenumber="37">
<thead>
<tr>
<th>Parameter</th>
<th>Required</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>EnableDiagnostics</strong></td>
<td>Required</td>
<td><code>boolean</code></td>
<td>Determines whether Diagnostics are enabled</td>
</tr>
</tbody>
</table>
<h2 id="example" sourcefile="V1/main/V1/ARCHIVE/Diagnostics configuration.md" sourcestartlinenumber="39" sourceendlinenumber="39">Example</h2>
<h3 id="retrieve-the-diagnostics-configuration" sourcefile="V1/main/V1/ARCHIVE/Diagnostics configuration.md" sourcestartlinenumber="41" sourceendlinenumber="41">Retrieve the diagnostics configuration</h3>
<p sourcefile="V1/main/V1/ARCHIVE/Diagnostics configuration.md" sourcestartlinenumber="43" sourceendlinenumber="43">Example using <code>curl</code>:</p>
<pre sourcefile="V1/main/V1/ARCHIVE/Diagnostics configuration.md" sourcestartlinenumber="45" sourceendlinenumber="47"><code class="lang-bash">curl -X GET &quot;http://localhost:{port}/api/v1/configuration/system/diagnostics&quot;
</code></pre><p sourcefile="V1/main/V1/ARCHIVE/Diagnostics configuration.md" sourcestartlinenumber="49" sourceendlinenumber="49">Sample output:</p>
<pre sourcefile="V1/main/V1/ARCHIVE/Diagnostics configuration.md" sourcestartlinenumber="51" sourceendlinenumber="55"><code class="lang-code">{
    &quot;enableDiagnostics&quot;: true
}
</code></pre><h2 id="rest-urls" sourcefile="V1/main/V1/ARCHIVE/Diagnostics configuration.md" sourcestartlinenumber="57" sourceendlinenumber="57">REST URLs</h2>
<table sourcefile="V1/main/V1/ARCHIVE/Diagnostics configuration.md" sourcestartlinenumber="59" sourceendlinenumber="62">
<thead>
<tr>
<th>Relative URL</th>
<th>HTTP verb</th>
<th>Action</th>
</tr>
</thead>
<tbody>
<tr>
<td>api/v1/configuration/system/diagnostics</td>
<td>GET</td>
<td>Gets the diagnostics configuration</td>
</tr>
<tr>
<td>api/v1/configuration/system/diagnostics</td>
<td>PUT</td>
<td>Replaces the existing diagnostics configuration</td>
</tr>
</tbody>
</table>
</article>
          </div>
          
          <div class="hidden-sm col-md-2" role="complementary">
            <div class="sideaffix">
              <div class="contribution">
                <ul class="nav">
                  <li>
                    <a href="https://github.com/osisoft/OSIsoft-Adapter/blob/master/V1/ARCHIVE/Diagnostics configuration.md/#L1" class="contribution-link">Improve this Doc</a>
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
