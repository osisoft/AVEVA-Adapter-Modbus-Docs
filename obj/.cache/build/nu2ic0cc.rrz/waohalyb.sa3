<!DOCTYPE html>
<!--[if IE]><![endif]-->
<html>
  
  <head>
    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1">
    <title>Health endpoint configuration </title>
    <meta name="viewport" content="width=device-width">
    <meta name="title" content="Health endpoint configuration ">
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
            <article class="content wrap" id="_content" data-uid="HealthEndpointConfiguration">
<h1 id="health-endpoint-configuration" sourcefile="V1/main/V1/Configuration/Health endpoint configuration.md" sourcestartlinenumber="5" sourceendlinenumber="5">Health endpoint configuration</h1>

<p sourcefile="V1/main/V1/Configuration/Health endpoint configuration.md" sourcestartlinenumber="7" sourceendlinenumber="8">You can configure OSIsoft adapters to produce and store health data at a designated health endpoint.
For more information about adapter health, see <a class="xref" href="../Health/Adapter%20health.html" data-raw-source="[Adapter health](xref:AdapterHealth)" sourcefile="V1/main/V1/Configuration/Health endpoint configuration.md" sourcestartlinenumber="8" sourceendlinenumber="8">Adapter health</a>.</p>
<h2 id="configure-health-endpoint" sourcefile="V1/main/V1/Configuration/Health endpoint configuration.md" sourcestartlinenumber="10" sourceendlinenumber="10">Configure health endpoint</h2>
<p sourcefile="V1/main/V1/Configuration/Health endpoint configuration.md" sourcestartlinenumber="12" sourceendlinenumber="12">A health endpoint designates an OMF endpoint where adapter health information is sent. You can configure multiple health endpoints.</p>
<ol sourcefile="V1/main/V1/Configuration/Health endpoint configuration.md" sourcestartlinenumber="14" sourceendlinenumber="40">
<li sourcefile="V1/main/V1/Configuration/Health endpoint configuration.md" sourcestartlinenumber="14" sourceendlinenumber="16">Using any text editor, create a file that contains one or more health endpoints in the JSON format.<ul sourcefile="V1/main/V1/Configuration/Health endpoint configuration.md" sourcestartlinenumber="15" sourceendlinenumber="16">
<li sourcefile="V1/main/V1/Configuration/Health endpoint configuration.md" sourcestartlinenumber="15" sourceendlinenumber="15">For content structure, see <a href="#examples" data-raw-source="[Examples](#examples)" sourcefile="V1/main/V1/Configuration/Health endpoint configuration.md" sourcestartlinenumber="15" sourceendlinenumber="15">Examples</a>.</li>
<li sourcefile="V1/main/V1/Configuration/Health endpoint configuration.md" sourcestartlinenumber="16" sourceendlinenumber="16">For a table of all available health endpoint parameters, see <a href="#health-endpoint-parameters" data-raw-source="[Health endpoint parameters](#health-endpoint-parameters)" sourcefile="V1/main/V1/Configuration/Health endpoint configuration.md" sourcestartlinenumber="16" sourceendlinenumber="16">Health endpoint parameters</a>.</li>
</ul>
</li>
<li sourcefile="V1/main/V1/Configuration/Health endpoint configuration.md" sourcestartlinenumber="17" sourceendlinenumber="17">Save the file. For example, <em>HealthEndpoints.json</em>.</li>
<li sourcefile="V1/main/V1/Configuration/Health endpoint configuration.md" sourcestartlinenumber="18" sourceendlinenumber="40"><p sourcefile="V1/main/V1/Configuration/Health endpoint configuration.md" sourcestartlinenumber="18" sourceendlinenumber="18">Use any of the <a class="xref" href="Configuration%20tools.html" data-raw-source="[Configuration tools](xref:ConfigurationTools)" sourcefile="V1/main/V1/Configuration/Health endpoint configuration.md" sourcestartlinenumber="18" sourceendlinenumber="18">Configuration tools</a> capable of making HTTP requests to run either a POST or PUT command to their appropriate endpoint.</p>
<p sourcefile="V1/main/V1/Configuration/Health endpoint configuration.md" sourcestartlinenumber="20" sourceendlinenumber="20"> <strong>Note:</strong> <code>5590</code> is the default port number. If you selected a different port number, replace it with that value.</p>
<ul sourcefile="V1/main/V1/Configuration/Health endpoint configuration.md" sourcestartlinenumber="22" sourceendlinenumber="40">
<li sourcefile="V1/main/V1/Configuration/Health endpoint configuration.md" sourcestartlinenumber="22" sourceendlinenumber="30"><p sourcefile="V1/main/V1/Configuration/Health endpoint configuration.md" sourcestartlinenumber="22" sourceendlinenumber="22"><strong>POST</strong> endpoint: <code>http://localhost:5590/api/v1/configuration/system/healthendpoints</code></p>
<p sourcefile="V1/main/V1/Configuration/Health endpoint configuration.md" sourcestartlinenumber="24" sourceendlinenumber="24">  Example using <code>curl</code>:</p>
<p sourcefile="V1/main/V1/Configuration/Health endpoint configuration.md" sourcestartlinenumber="26" sourceendlinenumber="26">  <strong>Note:</strong> Run this command from the same directory where the file is located.</p>
<pre sourcefile="V1/main/V1/Configuration/Health endpoint configuration.md" sourcestartlinenumber="28" sourceendlinenumber="30"><code class="lang-bash">curl -d &quot;@HealthEndpoints.json&quot; -H &quot;Content-Type: application/json&quot; -X POST &quot;http://localhost:5590/api/v1/configuration/system/healthendpoints&quot;
</code></pre></li>
<li sourcefile="V1/main/V1/Configuration/Health endpoint configuration.md" sourcestartlinenumber="32" sourceendlinenumber="40"><p sourcefile="V1/main/V1/Configuration/Health endpoint configuration.md" sourcestartlinenumber="32" sourceendlinenumber="32"><strong>PUT</strong> endpoint: <code>http://localhost:5590/api/v1/configuration/system/healthendpoints/{Id}</code></p>
<p sourcefile="V1/main/V1/Configuration/Health endpoint configuration.md" sourcestartlinenumber="34" sourceendlinenumber="34">  Example using <code>curl</code>:</p>
<p sourcefile="V1/main/V1/Configuration/Health endpoint configuration.md" sourcestartlinenumber="36" sourceendlinenumber="36">  <strong>Note:</strong> Run this command from the same directory where the file is located.</p>
<pre sourcefile="V1/main/V1/Configuration/Health endpoint configuration.md" sourcestartlinenumber="38" sourceendlinenumber="40"><code class="lang-bash">curl -d &quot;@HealthEndpoints.json&quot; -H &quot;Content-Type: application/json&quot; -X POST &quot;http://localhost:5590/api/v1/configuration/system/healthendpoints/OCS&quot;
</code></pre></li>
</ul>
</li>
</ol>
<h2 id="health-endpoints-schema" sourcefile="V1/main/V1/Configuration/Health endpoint configuration.md" sourcestartlinenumber="42" sourceendlinenumber="42">Health endpoints schema</h2>
<p sourcefile="V1/main/V1/Configuration/Health endpoint configuration.md" sourcestartlinenumber="44" sourceendlinenumber="44">The full schema definition for the health endpoint configuration is in the <em>System_HealthEndpoints_schema.json</em> file located in one of the folders listed below:</p>
<p sourcefile="V1/main/V1/Configuration/Health endpoint configuration.md" sourcestartlinenumber="46" sourceendlinenumber="46">Windows: <em>%ProgramFiles%\OSIsoft\Adapters\AdapterName\Schemas</em></p>
<p sourcefile="V1/main/V1/Configuration/Health endpoint configuration.md" sourcestartlinenumber="48" sourceendlinenumber="48">Linux: <em>/opt/OSIsoft/Adapters/AdapterName/Schemas</em></p>
<h2 id="health-endpoint-parameters" sourcefile="V1/main/V1/Configuration/Health endpoint configuration.md" sourcestartlinenumber="50" sourceendlinenumber="50">Health endpoint parameters</h2>
<p sourcefile="V1/main/V1/Configuration/Health endpoint configuration.md" sourcestartlinenumber="52" sourceendlinenumber="52">The following parameters are available for configuring health endpoints:</p>
<table sourcefile="V1/main/V1/Configuration/Health endpoint configuration.md" sourcestartlinenumber="54" sourceendlinenumber="63">
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
<td><strong>Id</strong></td>
<td>Optional</td>
<td><code>string</code></td>
<td>Uniquely identifies the endpoint. This can be any alphanumeric string. If left blank, a unique value is generated automatically.</td>
</tr>
<tr>
<td><strong>Endpoint</strong></td>
<td>Required</td>
<td><code>string</code></td>
<td>The URL of the OMF endpoint to receive this health data</td>
</tr>
<tr>
<td><strong>Username</strong></td>
<td>Required for PI Web API endpoints</td>
<td><code>string</code></td>
<td>The username used to authenticate with a PI Web API OMF endpoint</td>
</tr>
<tr>
<td><strong>Password</strong></td>
<td>Required for PI Web API endpoints</td>
<td><code>string</code></td>
<td>The password used to authenticate with a PI Web API OMF endpoint</td>
</tr>
<tr>
<td><strong>ClientId</strong></td>
<td>Required for OCS endpoints</td>
<td><code>string</code></td>
<td>The Client Id used for authentication with an OSIsoft Cloud Services OMF endpoint</td>
</tr>
<tr>
<td><strong>ClientSecret</strong></td>
<td>Required for OCS endpoints</td>
<td><code>string</code></td>
<td>The Client Secret used for authentication with an OSIsoft Cloud Services OMF endpoint</td>
</tr>
<tr>
<td><strong>TokenEndpoint</strong></td>
<td>Optional for OCS endpoints</td>
<td><code>string</code></td>
<td>Retrieves an OCS token from an alternative endpoint</td>
</tr>
<tr>
<td><strong>ValidateEndpointCertificate</strong></td>
<td>Optional</td>
<td><code>boolean</code></td>
<td>Disables verification of destination security certificate. Use for testing only with self-signed certificates; OSIsoft recommends keeping this set to the default, true, in production environments.</td>
</tr>
</tbody>
</table>
<h2 id="examples" sourcefile="V1/main/V1/Configuration/Health endpoint configuration.md" sourcestartlinenumber="65" sourceendlinenumber="65">Examples</h2>
<h3 id="ocs-endpoint" sourcefile="V1/main/V1/Configuration/Health endpoint configuration.md" sourcestartlinenumber="67" sourceendlinenumber="67">OCS endpoint</h3>
<pre sourcefile="V1/main/V1/Configuration/Health endpoint configuration.md" sourcestartlinenumber="69" sourceendlinenumber="76"><code class="lang-code">{
    &quot;Id&quot;: &quot;OCS&quot;,
    &quot;Endpoint&quot;: &quot;https://&lt;OCS OMF endpoint&gt;&quot;,
    &quot;ClientId&quot;: &quot;&lt;clientid&gt;&quot;,
    &quot;ClientSecret&quot;: &quot;&lt;clientsecret&gt;&quot;
}
</code></pre><h3 id="pi-web-api-endpoint" sourcefile="V1/main/V1/Configuration/Health endpoint configuration.md" sourcestartlinenumber="78" sourceendlinenumber="78">PI Web API endpoint</h3>
<pre sourcefile="V1/main/V1/Configuration/Health endpoint configuration.md" sourcestartlinenumber="80" sourceendlinenumber="87"><code class="lang-code">{
    &quot;Id&quot;: &quot;PI Web API&quot;,
    &quot;Endpoint&quot;: &quot;https://&lt;pi web api server&gt;/piwebapi/omf/&quot;,
    &quot;UserName&quot;: &quot;&lt;username&gt;&quot;,
    &quot;Password&quot;: &quot;&lt;password&gt;&quot;
}
</code></pre><h2 id="rest-urls" sourcefile="V1/main/V1/Configuration/Health endpoint configuration.md" sourcestartlinenumber="89" sourceendlinenumber="89">REST URLs</h2>
<table sourcefile="V1/main/V1/Configuration/Health endpoint configuration.md" sourcestartlinenumber="91" sourceendlinenumber="101">
<thead>
<tr>
<th>Relative URL</th>
<th>HTTP verb</th>
<th>Action</th>
</tr>
</thead>
<tbody>
<tr>
<td>api/v1/configuration/system/healthEndpoints</td>
<td>GET</td>
<td>Gets all configured health endpoints</td>
</tr>
<tr>
<td>api/v1/configuration/system/healthEndpoints</td>
<td>DELETE</td>
<td>Deletes all configured health endpoints</td>
</tr>
<tr>
<td>api/v1/configuration/system/healthEndpoints</td>
<td>POST</td>
<td>Adds an array of health endpoints or a single endpoint. Fails if any endpoint already exists</td>
</tr>
<tr>
<td>api/v1/configuration/system/healthEndpoints</td>
<td>PUT</td>
<td>Replaces all health endpoints. <strong>Note:</strong> Requires an array of endpoints</td>
</tr>
<tr>
<td>api/v1/configuration/system/healthEndpoints</td>
<td>PATCH</td>
<td>Allows partial updating of configured health endpoints<br><strong>Note:</strong> The request must be an array containing one or more health endpoints. Each health endpoint in the array must include its <em>Id</em>.</td>
</tr>
<tr>
<td>api/v1/configuration/system/healthEndpoints/<em>Id</em></td>
<td>GET</td>
<td>Gets configured health endpoint by <em>Id</em></td>
</tr>
<tr>
<td>api/v1/configuration/system/healthEndpoints/<em>Id</em></td>
<td>DELETE</td>
<td>Deletes configured health endpoint by <em>Id</em></td>
</tr>
<tr>
<td>api/v1/configuration/system/healthEndpoints/<em>Id</em></td>
<td>PUT</td>
<td>Updates or creates a new health endpoint with the specified <em>Id</em></td>
</tr>
<tr>
<td>api/v1/configuration/system/healthEndpoints/<em>Id</em></td>
<td>PATCH</td>
<td>Allows partial updating of configured health endpoint by <em>Id</em></td>
</tr>
</tbody>
</table>
<p sourcefile="V1/main/V1/Configuration/Health endpoint configuration.md" sourcestartlinenumber="103" sourceendlinenumber="103"><strong>Note:</strong> Replace <em>Id</em> with the Id of the health endpoint.</p>
</article>
          </div>
          
          <div class="hidden-sm col-md-2" role="complementary">
            <div class="sideaffix">
              <div class="contribution">
                <ul class="nav">
                  <li>
                    <a href="https://github.com/osisoft/OSIsoft-Adapter/blob/master/V1/Configuration/Health endpoint configuration.md/#L1" class="contribution-link">Improve this Doc</a>
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
