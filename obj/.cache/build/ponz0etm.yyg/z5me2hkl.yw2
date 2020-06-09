<!DOCTYPE html>
<!--[if IE]><![endif]-->
<html>
  
  <head>
    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1">
    <title>Logging configuration </title>
    <meta name="viewport" content="width=device-width">
    <meta name="title" content="Logging configuration ">
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
            <article class="content wrap" id="_content" data-uid="LoggingConfiguration">
<h1 id="logging-configuration" sourcefile="V1/main/V1/Configuration/Logging configuration.md" sourcestartlinenumber="5" sourceendlinenumber="5">Logging configuration</h1>

<p sourcefile="V1/main/V1/Configuration/Logging configuration.md" sourcestartlinenumber="7" sourceendlinenumber="7">OSIsoft adapters write daily log messages for the adapter, the system, and OMF egress to flat text files in the following locations:</p>
<p sourcefile="V1/main/V1/Configuration/Logging configuration.md" sourcestartlinenumber="9" sourceendlinenumber="9">• Windows: <em>%ProgramData%\OSIsoft\Adapters{AdapterInstance}\Logs</em></p>
<p sourcefile="V1/main/V1/Configuration/Logging configuration.md" sourcestartlinenumber="11" sourceendlinenumber="11">• Linux: <em>/usr/share/OSIsoft/Adapters/{AdapterInstance}/Logs</em></p>
<p sourcefile="V1/main/V1/Configuration/Logging configuration.md" sourcestartlinenumber="13" sourceendlinenumber="13">Each message in the log displays the message severity level, timestamp, and the message itself.</p>
<h2 id="configure-logging" sourcefile="V1/main/V1/Configuration/Logging configuration.md" sourcestartlinenumber="15" sourceendlinenumber="15">Configure logging</h2>
<p sourcefile="V1/main/V1/Configuration/Logging configuration.md" sourcestartlinenumber="17" sourceendlinenumber="17">Complete the following steps to change the logging configuration:</p>
<ol sourcefile="V1/main/V1/Configuration/Logging configuration.md" sourcestartlinenumber="19" sourceendlinenumber="37">
<li sourcefile="V1/main/V1/Configuration/Logging configuration.md" sourcestartlinenumber="19" sourceendlinenumber="21"><p sourcefile="V1/main/V1/Configuration/Logging configuration.md" sourcestartlinenumber="19" sourceendlinenumber="19">Using any text editor, create a file that contains the logging configuration in the JSON format.</p>
<ul sourcefile="V1/main/V1/Configuration/Logging configuration.md" sourcestartlinenumber="20" sourceendlinenumber="21">
<li sourcefile="V1/main/V1/Configuration/Logging configuration.md" sourcestartlinenumber="20" sourceendlinenumber="20">For content structure, see <a href="#example" data-raw-source="[Example](#example)" sourcefile="V1/main/V1/Configuration/Logging configuration.md" sourcestartlinenumber="20" sourceendlinenumber="20">Example</a>.</li>
<li sourcefile="V1/main/V1/Configuration/Logging configuration.md" sourcestartlinenumber="21" sourceendlinenumber="21">For all available parameters, see <a href="#logging-parameters" data-raw-source="[Logging parameters](#logging-parameters)" sourcefile="V1/main/V1/Configuration/Logging configuration.md" sourcestartlinenumber="21" sourceendlinenumber="21">Logging parameters</a>.</li>
</ul>
</li>
<li sourcefile="V1/main/V1/Configuration/Logging configuration.md" sourcestartlinenumber="23" sourceendlinenumber="23"><p sourcefile="V1/main/V1/Configuration/Logging configuration.md" sourcestartlinenumber="23" sourceendlinenumber="23">Save the file. For example, <em>Component_Logging.json</em>.</p>
</li>
<li sourcefile="V1/main/V1/Configuration/Logging configuration.md" sourcestartlinenumber="25" sourceendlinenumber="37"><p sourcefile="V1/main/V1/Configuration/Logging configuration.md" sourcestartlinenumber="25" sourceendlinenumber="25">Use any of the <a class="xref" href="Configuration%20tools.html" data-raw-source="[Configuration tools](xref:ConfigurationTools)" sourcefile="V1/main/V1/Configuration/Logging configuration.md" sourcestartlinenumber="25" sourceendlinenumber="25">Configuration tools</a> capable of making HTTP requests to run a <code>PUT</code> command with the contents of that file to the following endpoint: <code>http://localhost:5590/api/v1/configuration/&lt;ComponentId&gt;/Logging</code>.</p>
<p sourcefile="V1/main/V1/Configuration/Logging configuration.md" sourcestartlinenumber="27" sourceendlinenumber="27"> <strong>Note:</strong>  Replace <em>&lt;ComponentId&gt;</em> with the ComponentId of the adapter. For example, <em>OpcUa1</em>.</p>
<p sourcefile="V1/main/V1/Configuration/Logging configuration.md" sourcestartlinenumber="29" sourceendlinenumber="29"> <code>5590</code> is the default port number. If you selected a different port number, replace it with that value.</p>
<p sourcefile="V1/main/V1/Configuration/Logging configuration.md" sourcestartlinenumber="31" sourceendlinenumber="31"> Example using <code>curl</code>:</p>
<p sourcefile="V1/main/V1/Configuration/Logging configuration.md" sourcestartlinenumber="33" sourceendlinenumber="33"> <strong>Note:</strong> Run this command from the same directory where the file is located.</p>
<pre sourcefile="V1/main/V1/Configuration/Logging configuration.md" sourcestartlinenumber="35" sourceendlinenumber="37"><code class="lang-bash">curl -d &quot;@Component_Logging.json&quot; -H &quot;Content-Type: application/json&quot; -X PUT &quot;http://localhost:5590/api/v1/configuration/&lt;ComponentId&gt;/Logging&quot;
</code></pre></li>
</ol>
<p sourcefile="V1/main/V1/Configuration/Logging configuration.md" sourcestartlinenumber="39" sourceendlinenumber="39">On successful execution, the log-level change takes effect immediately during runtime. The other configurations (log file size and file count) are updated after the adapter is restarted.</p>
<p sourcefile="V1/main/V1/Configuration/Logging configuration.md" sourcestartlinenumber="41" sourceendlinenumber="41"><strong>Note:</strong>  Any parameter not specified in the updated configuration file reverts to the default schema value.</p>
<h2 id="logging-schema" sourcefile="V1/main/V1/Configuration/Logging configuration.md" sourcestartlinenumber="43" sourceendlinenumber="43">Logging schema</h2>
<p sourcefile="V1/main/V1/Configuration/Logging configuration.md" sourcestartlinenumber="45" sourceendlinenumber="45">The full schema definition for the logging configuration is in the component specific logging file: <em>AdapterName_Logging_schema.json</em>, <em>OmfEgress_Logging_schema.json</em>, or <em>System_Logging_schema.json</em> located in one of the folders listed below:</p>
<p sourcefile="V1/main/V1/Configuration/Logging configuration.md" sourcestartlinenumber="47" sourceendlinenumber="47">Windows: <em>%ProgramFiles%\OSIsoft\Adapters\AdapterName\Schemas</em></p>
<p sourcefile="V1/main/V1/Configuration/Logging configuration.md" sourcestartlinenumber="49" sourceendlinenumber="49">Linux: <em>/opt/OSIsoft/Adapters/AdapterName/Schemas</em></p>
<h2 id="logging-parameters" sourcefile="V1/main/V1/Configuration/Logging configuration.md" sourcestartlinenumber="51" sourceendlinenumber="51">Logging parameters</h2>
<p sourcefile="V1/main/V1/Configuration/Logging configuration.md" sourcestartlinenumber="53" sourceendlinenumber="53">The following parameters are available for configuring logging:</p>
<table sourcefile="V1/main/V1/Configuration/Logging configuration.md" sourcestartlinenumber="55" sourceendlinenumber="59">
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
<td><strong>logLevel</strong></td>
<td>Optional</td>
<td>reference</td>
<td>The logLevel sets the minimum severity for messages to be included in the logs. <br>Messages with a severity below the level set are not included. <br>The log levels in their increasing order of severity are as follows: Trace, Debug, Information, Warning, Error, Critical, None. <br>For detailed information about the logLevels, see <a href="#loglevel" data-raw-source="[LogLevel](#loglevel)" sourcefile="V1/main/V1/Configuration/Logging configuration.md" sourcestartlinenumber="57" sourceendlinenumber="57">LogLevel</a>.</td>
</tr>
<tr>
<td><strong>logFileSizeLimitBytes</strong></td>
<td>Optional</td>
<td><code>integer</code></td>
<td>The maximum size (in bytes) of log files that the service will create for the component. It must be a positive integer.</td>
</tr>
<tr>
<td><strong>logFileCountLimit</strong></td>
<td>Optional</td>
<td><code>integer</code></td>
<td>The maximum number of log files that the service will create for the component. It must be a positive integer.</td>
</tr>
</tbody>
</table>
<h3 id="loglevel" sourcefile="V1/main/V1/Configuration/Logging configuration.md" sourcestartlinenumber="61" sourceendlinenumber="61">LogLevel</h3>
<table sourcefile="V1/main/V1/Configuration/Logging configuration.md" sourcestartlinenumber="63" sourceendlinenumber="71">
<thead>
<tr>
<th>Level</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>Trace</td>
<td>Logs that contain the most detailed messages. These messages may contain sensitive application data like actual received values, which is why these messages should not be enabled in production environment.</td>
</tr>
<tr>
<td>Debug</td>
<td>Logs that can be used to troubleshoot data flow issues by recording metrics and detailed flow related information.</td>
</tr>
<tr>
<td>Information</td>
<td>Logs that track the general flow of the application. Any non-repetitive general information like the following can be useful for diagnosing potential application errors: <br> - Version information related to the software at startup <br> - External services used <br> - Data source connection string <br> - Number of measurements <br> - Egress URL <br> - Change of state “Starting” or “Stopping” <br> - Configuration</td>
</tr>
<tr>
<td>Warning</td>
<td>Logs that highlight an abnormal or unexpected event in the application flow that does not otherwise cause the application execution to stop. Warning messages can indicate an unconfigured data source state, that a communication with backup failover instance has been lost, an insecure communication channel in use, or any other event that could require attention, but that does not impact data flow.</td>
</tr>
<tr>
<td>Error</td>
<td>Logs that highlight when the current flow of execution is stopped due to a failure. These should indicate a failure in the current activity and not an application-wide failure. It can indicate an invalid configuration, unavailable external endpoint, internal flow error, and so on.</td>
</tr>
<tr>
<td>Critical</td>
<td>Logs that describe an unrecoverable application or system crash or a catastrophic failure that requires immediate attention. This can indicate application wide failures like beta timeout expired, unable to start self-hosted endpoint, unable to access vital resource (for example, Data Protection key file), and so on.</td>
</tr>
<tr>
<td>None</td>
<td>Logging is disabled for the given component.</td>
</tr>
</tbody>
</table>
<h2 id="example" sourcefile="V1/main/V1/Configuration/Logging configuration.md" sourcestartlinenumber="73" sourceendlinenumber="73">Example</h2>
<h3 id="default-logging-configuration" sourcefile="V1/main/V1/Configuration/Logging configuration.md" sourcestartlinenumber="75" sourceendlinenumber="75">Default logging configuration</h3>
<p sourcefile="V1/main/V1/Configuration/Logging configuration.md" sourcestartlinenumber="77" sourceendlinenumber="78">By default, logging captures Information, Warning, Error, and Critical messages in the message logs.
The following logging configuration is the default for a component on install:</p>
<pre sourcefile="V1/main/V1/Configuration/Logging configuration.md" sourcestartlinenumber="80" sourceendlinenumber="86"><code class="lang-json">{
  &quot;logLevel&quot;: &quot;Information&quot;,
  &quot;logFileSizeLimitBytes&quot;: 34636833,
  &quot;logFileCountLimit&quot;: 31
}
</code></pre><h2 id="rest-urls" sourcefile="V1/main/V1/Configuration/Logging configuration.md" sourcestartlinenumber="88" sourceendlinenumber="88">REST URLs</h2>
<table sourcefile="V1/main/V1/Configuration/Logging configuration.md" sourcestartlinenumber="90" sourceendlinenumber="95">
<thead>
<tr>
<th>Relative URL</th>
<th>HTTP verb</th>
<th>Action</th>
</tr>
</thead>
<tbody>
<tr>
<td>api/v1/configuration/System/Logging</td>
<td>GET</td>
<td>Retrieves the system logging configuration</td>
</tr>
<tr>
<td>api/v1/configuration/System/Logging</td>
<td>PUT</td>
<td>Updates the system logging configuration</td>
</tr>
<tr>
<td>api/v1/configuration/<em>ComponentId</em>/Logging</td>
<td>GET</td>
<td>Retrieves the logging configuration of the specified adapter component</td>
</tr>
<tr>
<td>api/v1/configuration/<em>ComponentId</em>/Logging</td>
<td>PUT</td>
<td>Updates the logging configuration of the specified adapter component</td>
</tr>
</tbody>
</table>
<p sourcefile="V1/main/V1/Configuration/Logging configuration.md" sourcestartlinenumber="97" sourceendlinenumber="97"><strong>Note:</strong> Replace <em>ComponentId</em> with the Id of your adapter component. For example, Modbus1 or OpcUa1.</p>
</article>
          </div>
          
          <div class="hidden-sm col-md-2" role="complementary">
            <div class="sideaffix">
              <div class="contribution">
                <ul class="nav">
                  <li>
                    <a href="https://github.com/osisoft/OSIsoft-Adapter/blob/master/V1/Configuration/Logging configuration.md/#L1" class="contribution-link">Improve this Doc</a>
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
