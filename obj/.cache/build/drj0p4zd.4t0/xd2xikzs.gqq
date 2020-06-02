<!DOCTYPE html>
<!--[if IE]><![endif]-->
<html>
  
  <head>
    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1">
    <title>System components configuration </title>
    <meta name="viewport" content="width=device-width">
    <meta name="title" content="System components configuration ">
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
            <article class="content wrap" id="_content" data-uid="SystemComponentsConfiguration">
<h1 id="system-components-configuration" sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="5" sourceendlinenumber="5">System components configuration</h1>

<p sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="7" sourceendlinenumber="7">OSIsoft adapters use JSON configuration files in a protected directory on Windows and Linux to store configuration that is read on startup. While the files are accessible to view, OSIsoft recommends that you use REST or the EdgeCmd utility for any changes you make to the files.</p>
<p sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="9" sourceendlinenumber="9">As part of making adapters as secure as possible, any passwords or secrets that you configure are stored in encrypted form where cryptographic key material is stored separately in a secure location. If you edit the files directly, the adapter may not work as expected.</p>
<p sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="11" sourceendlinenumber="11"><strong>Note:</strong> You can edit any single component or facet of the system individually using REST, but you can also configure the system as a whole with a single REST call.</p>
<h2 id="configure-system-components" sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="13" sourceendlinenumber="13">Configure system components</h2>
<p sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="15" sourceendlinenumber="15">The configuration of system components includes adding, updating, and deleting components.</p>
<h3 id="add-a-system-component" sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="17" sourceendlinenumber="17">Add a system component</h3>
<p sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="19" sourceendlinenumber="19">Complete the following steps to add a new component to the system:</p>
<ol sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="21" sourceendlinenumber="64">
<li sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="21" sourceendlinenumber="37"><p sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="21" sourceendlinenumber="21">Using any text editor, create a file that contains the component to be added to the system in the JSON format.</p>
<ul sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="23" sourceendlinenumber="37">
<li sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="23" sourceendlinenumber="23">For content structure, see <a href="#examples" data-raw-source="[Examples](#examples)" sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="23" sourceendlinenumber="23">Examples</a>.</li>
<li sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="24" sourceendlinenumber="37"><p sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="24" sourceendlinenumber="24">For a table of all available parameters, see <a href="#system-components-parameters" data-raw-source="[System components parameters](#system-components-parameters)" sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="24" sourceendlinenumber="24">System components parameters</a>.</p>
<p sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="26" sourceendlinenumber="26"><strong>Note:</strong> The OmfEgress component is required for this initial release for adapters to run. You can add additional components, but only a single OmfEgress component is supported.</p>
<p sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="28" sourceendlinenumber="28">The following example adds a Modbus TCP adapter:</p>
<pre sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="30" sourceendlinenumber="35"><code class="lang-json">  {
    &quot;ComponentId&quot;: &quot;Modbus1&quot;,
    &quot;ComponentType&quot;: &quot;Modbus&quot;
  }
</code></pre><p sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="37" sourceendlinenumber="37"><strong>Note:</strong> A unique ComponentId is necessary for each component in the system. This example uses the ComponentId Modbus1 since it is the first Modbus TCP adapter to be added.</p>
</li>
</ul>
</li>
<li sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="39" sourceendlinenumber="39"><p sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="39" sourceendlinenumber="39">Save the file. For example, <em>AddComponent.json</em>.</p>
</li>
<li sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="40" sourceendlinenumber="64"><p sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="40" sourceendlinenumber="40">Use any of the <a class="xref" href="Configuration%20tools.html" data-raw-source="[Configuration tools](xref:ConfigurationTools)" sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="40" sourceendlinenumber="40">Configuration tools</a> capable of making HTTP requests to run either a <code>POST</code> or <code>PUT</code> command to their appropriate endpoint.</p>
<p sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="42" sourceendlinenumber="42"> <strong>Note:</strong> <code>5590</code> is the default port number. If you selected a different port number, replace it with that value.</p>
<ul sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="44" sourceendlinenumber="64">
<li sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="44" sourceendlinenumber="52"><p sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="44" sourceendlinenumber="44"><strong>POST</strong> endpoint: <code>http://localhost:5590/api/v1/configuration/system/components</code></p>
<p sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="46" sourceendlinenumber="46">  Example using <code>curl</code>:</p>
<p sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="48" sourceendlinenumber="48">  <strong>Note:</strong> Run this command from the same directory where the file is located.</p>
<pre sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="50" sourceendlinenumber="52"><code class="lang-bash">curl -d &quot;@AddComponent.json&quot; -H &quot;Content-Type: application/json&quot; -X POST &quot;http://localhost:5590/api/v1/configuration/system/components&quot;
</code></pre></li>
<li sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="54" sourceendlinenumber="64"><p sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="54" sourceendlinenumber="54"><strong>PUT</strong> endpoint: <code>http://localhost:5590/api/v1/configuration/system/components/&lt;componentId&gt;</code></p>
<p sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="56" sourceendlinenumber="56">  Example using <code>curl</code>:</p>
<p sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="58" sourceendlinenumber="58">  <strong>Note:</strong> Run this command from the same directory where the file is located.</p>
<pre sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="60" sourceendlinenumber="62"><code class="lang-bash">curl -d &quot;@AddComponent.json&quot; -H &quot;Content-Type: application/json&quot; -X PUT &quot;http://localhost:5590/api/v1/configuration/system/components/Modbus1&quot;
</code></pre><p sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="64" sourceendlinenumber="64">After the curl command completes successfully, you can configure or use the new component.</p>
</li>
</ul>
</li>
</ol>
<h3 id="update-system-components" sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="66" sourceendlinenumber="66">Update system components</h3>
<p sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="68" sourceendlinenumber="68">Complete the following steps to update the system components. For example, by adding or deleting components.</p>
<ol sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="70" sourceendlinenumber="88">
<li sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="70" sourceendlinenumber="70"><p sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="70" sourceendlinenumber="70">Using any text editor, create a file that contains the current system components configuration. For information on how to retrieve the system components configuration, see <a href="#rest-urls" data-raw-source="[REST URLs](#rest-urls)" sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="70" sourceendlinenumber="70">REST URLs</a>.</p>
</li>
<li sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="72" sourceendlinenumber="74"><p sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="72" sourceendlinenumber="72">Delete or add components as you need.</p>
<p sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="74" sourceendlinenumber="74"> <strong>Note:</strong> You cannot delete the OmfEgress component.</p>
</li>
<li sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="76" sourceendlinenumber="76"><p sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="76" sourceendlinenumber="76">Save the file. For example,  <em>UpdateComponents.json</em></p>
</li>
<li sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="78" sourceendlinenumber="88"><p sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="78" sourceendlinenumber="78">Use any of the <a class="xref" href="Configuration%20tools.html" data-raw-source="[Configuration tools](xref:ConfigurationTools)" sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="78" sourceendlinenumber="78">Configuration tools</a> capable of making HTTP requests to run a <code>PUT</code> command with the contents of that file to the following endpoint: <code>http://localhost:5590/api/v1/configuration/system/components</code></p>
<p sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="80" sourceendlinenumber="80"> <strong>Note:</strong> <code>5590</code> is the default port number. If you selected a different port number, replace it with that value.</p>
<p sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="82" sourceendlinenumber="82"> Example using <code>curl</code>:</p>
<p sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="84" sourceendlinenumber="84"> <strong>Note:</strong> Run this command from the same directory where the file is located.</p>
<pre sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="86" sourceendlinenumber="88"><code class="lang-bash">curl -d &quot;@UpdateComponents.json&quot; -H &quot;Content-Type: application/json&quot; -X PUT &quot;http://localhost:5590/api/v1/configuration/system/components&quot;
</code></pre></li>
</ol>
<h3 id="delete-a-system-component" sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="90" sourceendlinenumber="90">Delete a system component</h3>
<p sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="92" sourceendlinenumber="92">Complete the following steps to delete an existing component:</p>
<ol sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="94" sourceendlinenumber="109">
<li sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="94" sourceendlinenumber="94"><p sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="94" sourceendlinenumber="94">Start any of the <a class="xref" href="Configuration%20tools.html" data-raw-source="[Configuration tools](xref:ConfigurationTools)" sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="94" sourceendlinenumber="94">Configuration tools</a> capable of making HTTP requests.</p>
</li>
<li sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="96" sourceendlinenumber="109"><p sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="96" sourceendlinenumber="96">Run a <code>DELETE</code> command to the following endpoint, replacing <code>&lt;ComponentId&gt;</code> with the ID of the component that you want to delete: <code>http://localhost:5590/api/v1/configuration/system/components/&lt;ComponentId&gt;/</code></p>
<p sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="98" sourceendlinenumber="98"> <strong>Note:</strong> <code>5590</code> is the default port number. If you selected a different port number, replace it with that value.</p>
<p sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="100" sourceendlinenumber="100"> Example using <code>curl</code>:</p>
<p sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="102" sourceendlinenumber="103"> <strong>Note:</strong> Run this command from the same directory where the file is located. <br>
 <em>Delete OpcUa1 component</em></p>
<pre sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="105" sourceendlinenumber="107"><code class="lang-bash">curl -X DELETE &quot;http://localhost:5590/api/v1/configuration/system/components/OpcUa1/&quot;
</code></pre><p sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="109" sourceendlinenumber="109"> All the logs and configurations files for the deleted components are moved to the corresponding <em>logs/Removed</em> or <em>Configuration/Removed</em> folder.</p>
</li>
</ol>
<h2 id="system-components-schema" sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="111" sourceendlinenumber="111">System components schema</h2>
<p sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="113" sourceendlinenumber="113">The full schema definition for the system components configuration is in the <em>System_Components_schema.json</em> file located in one of the folders listed below:</p>
<p sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="115" sourceendlinenumber="115">Windows: <em>%ProgramFiles%\OSIsoft\Adapters\AdapterName\Schemas</em></p>
<p sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="117" sourceendlinenumber="117">Linux: <em>/opt/OSIsoft/Adapters/AdapterName/Schemas</em></p>
<h2 id="system-components-parameters" sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="119" sourceendlinenumber="119">System components parameters</h2>
<p sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="121" sourceendlinenumber="121">The following parameters are available for configuring system components:</p>
<table sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="123" sourceendlinenumber="126">
<thead>
<tr>
<th>Parameters</th>
<th>Required</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>ComponentId</strong></td>
<td>Required</td>
<td><code>string</code></td>
<td>The ID of the component. It can be any alphanumeric string, for example OmfEgress. A properly configured ComponentID follows these rules:<br>Cannot contain leading or trailing space <br> Cannot use the following characters:<br> <code>&gt;</code> <code>&lt;</code> <code>/</code> <code>:</code> <code>?</code> <code>#</code> <code>[</code> <code>]</code> <code>@</code> <code>!</code> <code>$</code> <code>&amp;</code> <code>*</code> <code>\</code> <code>&quot;</code> <code>(</code> <code>)</code> <code>\\</code> <code>+</code> <code>,</code> <code>;</code> <code>=</code> <code>\|</code> <code>` </code> <code>{</code> <code>}</code></td>
</tr>
<tr>
<td><strong>ComponentType</strong></td>
<td>Required</td>
<td><code>string</code></td>
<td>The type of the component, for example OmfEgress. There are two types of components: OmfEgress and the adapter.</td>
</tr>
</tbody>
</table>
<h2 id="examples" sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="128" sourceendlinenumber="128">Examples</h2>
<h3 id="default-system-components-configuration" sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="130" sourceendlinenumber="130">Default system components configuration</h3>
<p sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="132" sourceendlinenumber="132">The default <em>System_Components.json</em> file for the System component contains the following information.</p>
<pre sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="134" sourceendlinenumber="141"><code class="lang-json">[
  {
    &quot;ComponentId&quot;: &quot;OmfEgress&quot;,
    &quot;ComponentType&quot;: &quot;OmfEgress&quot;
  }
]
</code></pre><h3 id="system-components-configuration-with-two-adapter-instances" sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="143" sourceendlinenumber="143">System components configuration with two adapter instances</h3>
<pre sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="145" sourceendlinenumber="160"><code class="lang-json">[
  {
                &quot;componentId&quot;: &quot;Modbus1&quot;,
                &quot;componentType&quot;: &quot;Modbus&quot;
            },
            {
                &quot;componentId&quot;: &quot;Modbus2&quot;,
                &quot;componentType&quot;: &quot;Modbus&quot;
            },
            {
                &quot;ComponentId&quot;: &quot;OmfEgress&quot;,
                &quot;ComponentType&quot;: &quot;OmfEgress&quot;
   }
]
</code></pre><h2 id="rest-urls" sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="162" sourceendlinenumber="162">REST URLs</h2>
<table sourcefile="V1/main/V1/Configuration/System components configuration.md" sourcestartlinenumber="164" sourceendlinenumber="170">
<thead>
<tr>
<th>Relative URL</th>
<th>HTTP verb</th>
<th>Action</th>
</tr>
</thead>
<tbody>
<tr>
<td>api/v1/configuration/system/components</td>
<td>GET</td>
<td>Retrieves  the system components configuration</td>
</tr>
<tr>
<td>api/v1/configuration/system/components</td>
<td>POST</td>
<td>Adds a new component to the system configuration</td>
</tr>
<tr>
<td>api/v1/configuration/system/components</td>
<td>PUT</td>
<td>Updates the system components configuration</td>
</tr>
<tr>
<td>api/v1/configuration/system/components/<em>componentId</em></td>
<td>DELETE</td>
<td>Deletes a specific component from the system components configuration</td>
</tr>
<tr>
<td>api/v1/configuration/system/components/<em>componentId</em></td>
<td>PUT</td>
<td>Creates a new component with the specified <em>componentId</em> in the system configuration</td>
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
                    <a href="https://github.com/osisoft/OSIsoft-Adapter/blob/master/V1/Configuration/System components configuration.md/#L1" class="contribution-link">Improve this Doc</a>
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
