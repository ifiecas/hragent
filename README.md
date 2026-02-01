<section>
  <h1>Self-Service Employment Certificate Generator</h1>

  <p>
    This repository contains a Copilot Studio HR agent that generates employment certificates using AI,
    grounded in company data stored in SharePoint.
  </p>

  <p>
    The goal of this project is to show how AI can help pre-fill business documents while keeping all factual
    information controlled, accurate, and safe for real-world use.
  </p>

  <h2>What This Does</h2>
  <p>This HR agent lets employees generate their own employment certificate in minutes.</p>
  <ul>
    <li>No HR emails</li>
    <li>No manual document editing</li>
    <li>No waiting</li>
  </ul>

  <p>
    AI helps with wording and structure, while employee data comes from a SharePoint list as the single source of truth.
  </p>

  <h2>How It Works</h2>
  <p>An employee opens the HR agent and requests an employment certificate.</p>

  <p>The system:</p>
  <ol>
    <li>Identifies the logged-in user</li>
    <li>Looks up employee details in SharePoint</li>
    <li>Uses AI to generate the document wording</li>
    <li>Pre-fills a fixed Word template</li>
    <li>Converts the document to PDF</li>
    <li>Returns a download link</li>
  </ol>

  <p>All of this happens in one automated flow.</p>

  <h2>Architecture</h2>
  <p>At a high level, the flow looks like this:</p>

  <pre><code>Copilot Studio (HR Agent)
  → Power Automate
  → SharePoint List (Employee Data)
  → Word Template (Pre-fill)
  → PDF Conversion
  → SharePoint Library
  → Download Link returned to Copilot</code></pre>

  <p>
    SharePoint is the source of truth.<br>
    AI never invents employee information.
  </p>

  <h2>Key Principles</h2>
  <ul>
    <li>AI is used for structure and wording only</li>
    <li>All employee data is retrieved from SharePoint</li>
    <li>Documents always follow a fixed template</li>
    <li>Output is consistent and company-ready</li>
  </ul>

  <p>This keeps AI-generated documents controlled and reliable.</p>

  <h2>What’s Included</h2>
  <ul>
    <li>Copilot Studio package export</li>
    <li>Power Automate flow definitions</li>
    <li>Example SharePoint list schema</li>
    <li>Sample Word employment certificate template</li>
  </ul>

  <h2>Where This Pattern Applies</h2>
  <p>This same approach works for any document that is created regularly using a template, such as:</p>
  <ul>
    <li>Employment certificates</li>
    <li>Contracts</li>
    <li>Statements of work</li>
    <li>Invoices</li>
    <li>Internal letters</li>
    <li>Newsletters</li>
  </ul>

  <p>
    Once the structure and data sources are in place, AI can help generate documents at scale.
  </p>

  <h2>Notes</h2>
  <ul>
    <li>Employee data in this repo is simulated</li>
    <li>Templates can be replaced with company-branded versions</li>
    <li>Approval steps and signatures can be added if needed</li>
  </ul>

  <h2>Credits</h2>
  <p>
    Inspired by Matthew Devaney’s talk on grounding AI-generated documents in company data:
    <a href="https://www.youtube.com/watch?v=g6SsJdbgSeM">https://www.youtube.com/watch?v=g6SsJdbgSeM</a>
  </p>
</section>
