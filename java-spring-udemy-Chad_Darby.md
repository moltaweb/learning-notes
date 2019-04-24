





<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
  <link rel="dns-prefetch" href="https://github.githubassets.com">
  <link rel="dns-prefetch" href="https://avatars0.githubusercontent.com">
  <link rel="dns-prefetch" href="https://avatars1.githubusercontent.com">
  <link rel="dns-prefetch" href="https://avatars2.githubusercontent.com">
  <link rel="dns-prefetch" href="https://avatars3.githubusercontent.com">
  <link rel="dns-prefetch" href="https://github-cloud.s3.amazonaws.com">
  <link rel="dns-prefetch" href="https://user-images.githubusercontent.com/">



  <link crossorigin="anonymous" media="all" integrity="sha512-OBabailf0Gja8rWVZO1xyYAw//CQdLOJF4riG050gTxsVqVD7az4Sq56hPWfv3AoaxuEhYXgQlGQcNxzZzDyVA==" rel="stylesheet" href="https://github.githubassets.com/assets/frameworks-d69542a4a3958db914b3bec3f757de26.css" />
  
    <link crossorigin="anonymous" media="all" integrity="sha512-9JYhI94ytOGj9ys2NPH/dLmDYt5gvOTDsTuEP25VJM20DiU2QauyCBvl25h23d5qMa4DMaRG9t20oJs2sI/9yA==" rel="stylesheet" href="https://github.githubassets.com/assets/github-e6824a31db0aee268e9c71b6f3195e35.css" />
    
    
    
    

  <meta name="viewport" content="width=device-width">
  
  <title>cursos/udemy-spring-mvc-chaddarby.md at master · moltaweb/cursos</title>
    <meta name="description" content="Apuntes de los cursos (Privado). Contribute to moltaweb/cursos development by creating an account on GitHub.">
    <link rel="search" type="application/opensearchdescription+xml" href="/opensearch.xml" title="GitHub">
  <link rel="fluid-icon" href="https://github.com/fluidicon.png" title="GitHub">
  <meta property="fb:app_id" content="1401488693436528">

    <meta name="twitter:image:src" content="https://avatars3.githubusercontent.com/u/20514020?s=400&amp;v=4" /><meta name="twitter:site" content="@github" /><meta name="twitter:card" content="summary" /><meta name="twitter:title" content="moltaweb/cursos" /><meta name="twitter:description" content="Apuntes de los cursos (Privado). Contribute to moltaweb/cursos development by creating an account on GitHub." />
    <meta property="og:image" content="https://avatars3.githubusercontent.com/u/20514020?s=400&amp;v=4" /><meta property="og:site_name" content="GitHub" /><meta property="og:type" content="object" /><meta property="og:title" content="moltaweb/cursos" /><meta property="og:url" content="https://github.com/moltaweb/cursos" /><meta property="og:description" content="Apuntes de los cursos (Privado). Contribute to moltaweb/cursos development by creating an account on GitHub." />

  <link rel="assets" href="https://github.githubassets.com/">
  <link rel="web-socket" href="wss://live.github.com/_sockets/VjI6Mzk2ODc5MjkzOjQxODNiN2NmODM2MmI2OWRhODRjOWIwZDYxNjNhMjVjMzM0Yjk2ZTM1YmYzOWUzNjAyYjg2NDY3ZDJjZjNmYjI=--a9203339568ee991b1404bed1384f7aa02e8b605">
  <meta name="pjax-timeout" content="1000">
  <link rel="sudo-modal" href="/sessions/sudo_modal">
  <meta name="request-id" content="8F1E:38C41:A43FA3:F7AD76:5CC06BEB" data-pjax-transient>


  

  <meta name="selected-link" value="repo_source" data-pjax-transient>

      <meta name="google-site-verification" content="KT5gs8h0wvaagLKAVWq8bbeNwnZZK1r1XQysX3xurLU">
    <meta name="google-site-verification" content="ZzhVyEFwb7w3e0-uOTltm8Jsck2F5StVihD0exw2fsA">
    <meta name="google-site-verification" content="GXs5KoUUkNCoaAZn7wPN-t01Pywp9M3sEjnt_3_ZWPc">

  <meta name="octolytics-host" content="collector.githubapp.com" /><meta name="octolytics-app-id" content="github" /><meta name="octolytics-event-url" content="https://collector.githubapp.com/github-external/browser_event" /><meta name="octolytics-dimension-request_id" content="8F1E:38C41:A43FA3:F7AD76:5CC06BEB" /><meta name="octolytics-dimension-region_edge" content="ams" /><meta name="octolytics-dimension-region_render" content="iad" /><meta name="octolytics-actor-id" content="20514020" /><meta name="octolytics-actor-login" content="moltaweb" /><meta name="octolytics-actor-hash" content="a413d0ae8a8480f886cb6d5cda765e3d115bbb799de7f1b143ede54809f3459c" />
<meta name="analytics-location" content="/&lt;user-name&gt;/&lt;repo-name&gt;/blob/show" data-pjax-transient="true" />



    <meta name="google-analytics" content="UA-3769691-2">

  <meta class="js-ga-set" name="userId" content="0cfaa588ccaea4c0d1acd117553dcca6">

<meta class="js-ga-set" name="dimension1" content="Logged In">



  

      <meta name="hostname" content="github.com">
    <meta name="user-login" content="moltaweb">

      <meta name="expected-hostname" content="github.com">
    <meta name="js-proxy-site-detection-payload" content="YmQ3Mzg3YTY0YTlhZDU3MDEwMmJlZDM2M2M0ZjNlY2FlYzYxNTI1NmFmMWFmZjJhY2E3MTVhMjBkODAwMjkwM3x7InJlbW90ZV9hZGRyZXNzIjoiOTMuMTc2LjEyOC4yMiIsInJlcXVlc3RfaWQiOiI4RjFFOjM4QzQxOkE0M0ZBMzpGN0FENzY6NUNDMDZCRUIiLCJ0aW1lc3RhbXAiOjE1NTYxMTQ0MTYsImhvc3QiOiJnaXRodWIuY29tIn0=">

    <meta name="enabled-features" content="UNIVERSE_BANNER,MARKETPLACE_INVOICED_BILLING,MARKETPLACE_SOCIAL_PROOF_CUSTOMERS,MARKETPLACE_TRENDING_SOCIAL_PROOF,MARKETPLACE_RECOMMENDATIONS,NOTIFY_ON_BLOCK,RELATED_ISSUES">

  <meta name="html-safe-nonce" content="a7fe00e3463879cfc346b37ba4944b9d29098cf6">

  <meta http-equiv="x-pjax-version" content="809a659e00f4f7e77d896aff94d8b9e6">
  

      <link href="https://github.com/moltaweb/cursos/commits/master.atom?token=AE4QJZHPSC3H2IXVOBGDP652ZWWIA" rel="alternate" title="Recent Commits to cursos:master" type="application/atom+xml">

  <meta name="go-import" content="github.com/moltaweb/cursos git https://github.com/moltaweb/cursos.git">

  <meta name="octolytics-dimension-user_id" content="20514020" /><meta name="octolytics-dimension-user_login" content="moltaweb" /><meta name="octolytics-dimension-repository_id" content="182517889" /><meta name="octolytics-dimension-repository_nwo" content="moltaweb/cursos" /><meta name="octolytics-dimension-repository_public" content="false" /><meta name="octolytics-dimension-repository_is_fork" content="false" /><meta name="octolytics-dimension-repository_network_root_id" content="182517889" /><meta name="octolytics-dimension-repository_network_root_nwo" content="moltaweb/cursos" /><meta name="octolytics-dimension-repository_explore_github_marketplace_ci_cta_shown" content="true" />


    <link rel="canonical" href="https://github.com/moltaweb/cursos/blob/master/udemy-spring-mvc-chaddarby.md" data-pjax-transient>


  <meta name="browser-stats-url" content="https://api.github.com/_private/browser/stats">

  <meta name="browser-errors-url" content="https://api.github.com/_private/browser/errors">

  <link rel="mask-icon" href="https://github.githubassets.com/pinned-octocat.svg" color="#000000">
  <link rel="icon" type="image/x-icon" class="js-site-favicon" href="https://github.githubassets.com/favicon.ico">

<meta name="theme-color" content="#1e2327">




  <link rel="manifest" href="/manifest.json" crossOrigin="use-credentials">

  </head>

  <body class="logged-in env-production page-responsive min-width-0 page-blob">
    

  <div class="position-relative js-header-wrapper ">
    <a href="#start-of-content" tabindex="1" class="p-3 bg-blue text-white show-on-focus js-skip-to-content">Skip to content</a>
    <div id="js-pjax-loader-bar" class="pjax-loader-bar"><div class="progress"></div></div>

    
    
    


          <header class="Header js-details-container Details flex-wrap flex-lg-nowrap p-responsive" role="banner">

    <div class="Header-item d-none d-lg-flex">
      <a class="Header-link" href="https://github.com/" data-hotkey="g d" aria-label="Homepage" data-ga-click="Header, go to dashboard, icon:logo">
  <svg class="octicon octicon-mark-github v-align-middle" height="32" viewBox="0 0 16 16" version="1.1" width="32" aria-hidden="true"><path fill-rule="evenodd" d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.013 8.013 0 0 0 16 8c0-4.42-3.58-8-8-8z"/></svg>
</a>

    </div>

    <div class="Header-item d-lg-none">
      <button class="Header-link btn-link mt-1 js-details-target" type="button" aria-label="Toggle navigation" aria-expanded="false">
        <svg height="24" class="octicon octicon-three-bars" viewBox="0 0 12 16" version="1.1" width="18" aria-hidden="true"><path fill-rule="evenodd" d="M11.41 9H.59C0 9 0 8.59 0 8c0-.59 0-1 .59-1H11.4c.59 0 .59.41.59 1 0 .59 0 1-.59 1h.01zm0-4H.59C0 5 0 4.59 0 4c0-.59 0-1 .59-1H11.4c.59 0 .59.41.59 1 0 .59 0 1-.59 1h.01zM.59 11H11.4c.59 0 .59.41.59 1 0 .59 0 1-.59 1H.59C0 13 0 12.59 0 12c0-.59 0-1 .59-1z"/></svg>
      </button>
    </div>

    <div class="Header-item Header-item--full flex-column flex-lg-row width-full flex-order-2 flex-lg-order-none mr-0 mr-lg-3 mt-3 mt-lg-0 Details-content--hidden">
        <div class="header-search flex-self-stretch flex-lg-self-auto mr-0 mr-lg-3 mb-3 mb-lg-0 scoped-search site-scoped-search js-site-search position-relative js-jump-to"
  role="combobox"
  aria-owns="jump-to-results"
  aria-label="Search or jump to"
  aria-haspopup="listbox"
  aria-expanded="false"
>
  <div class="position-relative">
    <!-- '"` --><!-- </textarea></xmp> --></option></form><form class="js-site-search-form" role="search" aria-label="Site" data-scope-type="Repository" data-scope-id="182517889" data-scoped-search-url="/moltaweb/cursos/search" data-unscoped-search-url="/search" action="/moltaweb/cursos/search" accept-charset="UTF-8" method="get"><input name="utf8" type="hidden" value="&#x2713;" />
      <label class="form-control input-sm header-search-wrapper p-0 header-search-wrapper-jump-to position-relative d-flex flex-justify-between flex-items-center js-chromeless-input-container">
        <input type="text"
          class="form-control input-sm header-search-input jump-to-field js-jump-to-field js-site-search-focus js-site-search-field is-clearable"
          data-hotkey="s,/"
          name="q"
          value=""
          placeholder="Search or jump to…"
          data-unscoped-placeholder="Search or jump to…"
          data-scoped-placeholder="Search or jump to…"
          autocapitalize="off"
          aria-autocomplete="list"
          aria-controls="jump-to-results"
          aria-label="Search or jump to…"
          data-jump-to-suggestions-path="/_graphql/GetSuggestedNavigationDestinations#csrf-token=uQPQducRO7dRTlRAkbS1C6xw5RjguMeQMFQHmVBw9nKOu7ORReuuO3ZMhZXN+PpgcMuFzRG6hbXc1DARfrsZXg=="
          spellcheck="false"
          autocomplete="off"
          >
          <input type="hidden" class="js-site-search-type-field" name="type" >
            <img src="https://github.githubassets.com/images/search-key-slash.svg" alt="" class="mr-2 header-search-key-slash">

            <div class="Box position-absolute overflow-hidden d-none jump-to-suggestions js-jump-to-suggestions-container">
              
<ul class="d-none js-jump-to-suggestions-template-container">
  

<li class="d-flex flex-justify-start flex-items-center p-0 f5 navigation-item js-navigation-item js-jump-to-suggestion" role="option">
  <a tabindex="-1" class="no-underline d-flex flex-auto flex-items-center jump-to-suggestions-path js-jump-to-suggestion-path js-navigation-open p-2" href="">
    <div class="jump-to-octicon js-jump-to-octicon flex-shrink-0 mr-2 text-center d-none">
      <svg height="16" width="16" class="octicon octicon-repo flex-shrink-0 js-jump-to-octicon-repo d-none" title="Repository" aria-label="Repository" viewBox="0 0 12 16" version="1.1" role="img"><path fill-rule="evenodd" d="M4 9H3V8h1v1zm0-3H3v1h1V6zm0-2H3v1h1V4zm0-2H3v1h1V2zm8-1v12c0 .55-.45 1-1 1H6v2l-1.5-1.5L3 16v-2H1c-.55 0-1-.45-1-1V1c0-.55.45-1 1-1h10c.55 0 1 .45 1 1zm-1 10H1v2h2v-1h3v1h5v-2zm0-10H2v9h9V1z"/></svg>
      <svg height="16" width="16" class="octicon octicon-project flex-shrink-0 js-jump-to-octicon-project d-none" title="Project" aria-label="Project" viewBox="0 0 15 16" version="1.1" role="img"><path fill-rule="evenodd" d="M10 12h3V2h-3v10zm-4-2h3V2H6v8zm-4 4h3V2H2v12zm-1 1h13V1H1v14zM14 0H1a1 1 0 0 0-1 1v14a1 1 0 0 0 1 1h13a1 1 0 0 0 1-1V1a1 1 0 0 0-1-1z"/></svg>
      <svg height="16" width="16" class="octicon octicon-search flex-shrink-0 js-jump-to-octicon-search d-none" title="Search" aria-label="Search" viewBox="0 0 16 16" version="1.1" role="img"><path fill-rule="evenodd" d="M15.7 13.3l-3.81-3.83A5.93 5.93 0 0 0 13 6c0-3.31-2.69-6-6-6S1 2.69 1 6s2.69 6 6 6c1.3 0 2.48-.41 3.47-1.11l3.83 3.81c.19.2.45.3.7.3.25 0 .52-.09.7-.3a.996.996 0 0 0 0-1.41v.01zM7 10.7c-2.59 0-4.7-2.11-4.7-4.7 0-2.59 2.11-4.7 4.7-4.7 2.59 0 4.7 2.11 4.7 4.7 0 2.59-2.11 4.7-4.7 4.7z"/></svg>
    </div>

    <img class="avatar mr-2 flex-shrink-0 js-jump-to-suggestion-avatar d-none" alt="" aria-label="Team" src="" width="28" height="28">

    <div class="jump-to-suggestion-name js-jump-to-suggestion-name flex-auto overflow-hidden text-left no-wrap css-truncate css-truncate-target">
    </div>

    <div class="border rounded-1 flex-shrink-0 bg-gray px-1 text-gray-light ml-1 f6 d-none js-jump-to-badge-search">
      <span class="js-jump-to-badge-search-text-default d-none" aria-label="in this repository">
        In this repository
      </span>
      <span class="js-jump-to-badge-search-text-global d-none" aria-label="in all of GitHub">
        All GitHub
      </span>
      <span aria-hidden="true" class="d-inline-block ml-1 v-align-middle">↵</span>
    </div>

    <div aria-hidden="true" class="border rounded-1 flex-shrink-0 bg-gray px-1 text-gray-light ml-1 f6 d-none d-on-nav-focus js-jump-to-badge-jump">
      Jump to
      <span class="d-inline-block ml-1 v-align-middle">↵</span>
    </div>
  </a>
</li>

</ul>

<ul class="d-none js-jump-to-no-results-template-container">
  <li class="d-flex flex-justify-center flex-items-center f5 d-none js-jump-to-suggestion p-2">
    <span class="text-gray">No suggested jump to results</span>
  </li>
</ul>

<ul id="jump-to-results" role="listbox" class="p-0 m-0 js-navigation-container jump-to-suggestions-results-container js-jump-to-suggestions-results-container">
  

<li class="d-flex flex-justify-start flex-items-center p-0 f5 navigation-item js-navigation-item js-jump-to-scoped-search d-none" role="option">
  <a tabindex="-1" class="no-underline d-flex flex-auto flex-items-center jump-to-suggestions-path js-jump-to-suggestion-path js-navigation-open p-2" href="">
    <div class="jump-to-octicon js-jump-to-octicon flex-shrink-0 mr-2 text-center d-none">
      <svg height="16" width="16" class="octicon octicon-repo flex-shrink-0 js-jump-to-octicon-repo d-none" title="Repository" aria-label="Repository" viewBox="0 0 12 16" version="1.1" role="img"><path fill-rule="evenodd" d="M4 9H3V8h1v1zm0-3H3v1h1V6zm0-2H3v1h1V4zm0-2H3v1h1V2zm8-1v12c0 .55-.45 1-1 1H6v2l-1.5-1.5L3 16v-2H1c-.55 0-1-.45-1-1V1c0-.55.45-1 1-1h10c.55 0 1 .45 1 1zm-1 10H1v2h2v-1h3v1h5v-2zm0-10H2v9h9V1z"/></svg>
      <svg height="16" width="16" class="octicon octicon-project flex-shrink-0 js-jump-to-octicon-project d-none" title="Project" aria-label="Project" viewBox="0 0 15 16" version="1.1" role="img"><path fill-rule="evenodd" d="M10 12h3V2h-3v10zm-4-2h3V2H6v8zm-4 4h3V2H2v12zm-1 1h13V1H1v14zM14 0H1a1 1 0 0 0-1 1v14a1 1 0 0 0 1 1h13a1 1 0 0 0 1-1V1a1 1 0 0 0-1-1z"/></svg>
      <svg height="16" width="16" class="octicon octicon-search flex-shrink-0 js-jump-to-octicon-search d-none" title="Search" aria-label="Search" viewBox="0 0 16 16" version="1.1" role="img"><path fill-rule="evenodd" d="M15.7 13.3l-3.81-3.83A5.93 5.93 0 0 0 13 6c0-3.31-2.69-6-6-6S1 2.69 1 6s2.69 6 6 6c1.3 0 2.48-.41 3.47-1.11l3.83 3.81c.19.2.45.3.7.3.25 0 .52-.09.7-.3a.996.996 0 0 0 0-1.41v.01zM7 10.7c-2.59 0-4.7-2.11-4.7-4.7 0-2.59 2.11-4.7 4.7-4.7 2.59 0 4.7 2.11 4.7 4.7 0 2.59-2.11 4.7-4.7 4.7z"/></svg>
    </div>

    <img class="avatar mr-2 flex-shrink-0 js-jump-to-suggestion-avatar d-none" alt="" aria-label="Team" src="" width="28" height="28">

    <div class="jump-to-suggestion-name js-jump-to-suggestion-name flex-auto overflow-hidden text-left no-wrap css-truncate css-truncate-target">
    </div>

    <div class="border rounded-1 flex-shrink-0 bg-gray px-1 text-gray-light ml-1 f6 d-none js-jump-to-badge-search">
      <span class="js-jump-to-badge-search-text-default d-none" aria-label="in this repository">
        In this repository
      </span>
      <span class="js-jump-to-badge-search-text-global d-none" aria-label="in all of GitHub">
        All GitHub
      </span>
      <span aria-hidden="true" class="d-inline-block ml-1 v-align-middle">↵</span>
    </div>

    <div aria-hidden="true" class="border rounded-1 flex-shrink-0 bg-gray px-1 text-gray-light ml-1 f6 d-none d-on-nav-focus js-jump-to-badge-jump">
      Jump to
      <span class="d-inline-block ml-1 v-align-middle">↵</span>
    </div>
  </a>
</li>

  

<li class="d-flex flex-justify-start flex-items-center p-0 f5 navigation-item js-navigation-item js-jump-to-global-search d-none" role="option">
  <a tabindex="-1" class="no-underline d-flex flex-auto flex-items-center jump-to-suggestions-path js-jump-to-suggestion-path js-navigation-open p-2" href="">
    <div class="jump-to-octicon js-jump-to-octicon flex-shrink-0 mr-2 text-center d-none">
      <svg height="16" width="16" class="octicon octicon-repo flex-shrink-0 js-jump-to-octicon-repo d-none" title="Repository" aria-label="Repository" viewBox="0 0 12 16" version="1.1" role="img"><path fill-rule="evenodd" d="M4 9H3V8h1v1zm0-3H3v1h1V6zm0-2H3v1h1V4zm0-2H3v1h1V2zm8-1v12c0 .55-.45 1-1 1H6v2l-1.5-1.5L3 16v-2H1c-.55 0-1-.45-1-1V1c0-.55.45-1 1-1h10c.55 0 1 .45 1 1zm-1 10H1v2h2v-1h3v1h5v-2zm0-10H2v9h9V1z"/></svg>
      <svg height="16" width="16" class="octicon octicon-project flex-shrink-0 js-jump-to-octicon-project d-none" title="Project" aria-label="Project" viewBox="0 0 15 16" version="1.1" role="img"><path fill-rule="evenodd" d="M10 12h3V2h-3v10zm-4-2h3V2H6v8zm-4 4h3V2H2v12zm-1 1h13V1H1v14zM14 0H1a1 1 0 0 0-1 1v14a1 1 0 0 0 1 1h13a1 1 0 0 0 1-1V1a1 1 0 0 0-1-1z"/></svg>
      <svg height="16" width="16" class="octicon octicon-search flex-shrink-0 js-jump-to-octicon-search d-none" title="Search" aria-label="Search" viewBox="0 0 16 16" version="1.1" role="img"><path fill-rule="evenodd" d="M15.7 13.3l-3.81-3.83A5.93 5.93 0 0 0 13 6c0-3.31-2.69-6-6-6S1 2.69 1 6s2.69 6 6 6c1.3 0 2.48-.41 3.47-1.11l3.83 3.81c.19.2.45.3.7.3.25 0 .52-.09.7-.3a.996.996 0 0 0 0-1.41v.01zM7 10.7c-2.59 0-4.7-2.11-4.7-4.7 0-2.59 2.11-4.7 4.7-4.7 2.59 0 4.7 2.11 4.7 4.7 0 2.59-2.11 4.7-4.7 4.7z"/></svg>
    </div>

    <img class="avatar mr-2 flex-shrink-0 js-jump-to-suggestion-avatar d-none" alt="" aria-label="Team" src="" width="28" height="28">

    <div class="jump-to-suggestion-name js-jump-to-suggestion-name flex-auto overflow-hidden text-left no-wrap css-truncate css-truncate-target">
    </div>

    <div class="border rounded-1 flex-shrink-0 bg-gray px-1 text-gray-light ml-1 f6 d-none js-jump-to-badge-search">
      <span class="js-jump-to-badge-search-text-default d-none" aria-label="in this repository">
        In this repository
      </span>
      <span class="js-jump-to-badge-search-text-global d-none" aria-label="in all of GitHub">
        All GitHub
      </span>
      <span aria-hidden="true" class="d-inline-block ml-1 v-align-middle">↵</span>
    </div>

    <div aria-hidden="true" class="border rounded-1 flex-shrink-0 bg-gray px-1 text-gray-light ml-1 f6 d-none d-on-nav-focus js-jump-to-badge-jump">
      Jump to
      <span class="d-inline-block ml-1 v-align-middle">↵</span>
    </div>
  </a>
</li>


    <li class="d-flex flex-justify-center flex-items-center p-0 f5 js-jump-to-suggestion">
      <img src="https://github.githubassets.com/images/spinners/octocat-spinner-128.gif" alt="Octocat Spinner Icon" class="m-2" width="28">
    </li>
</ul>

            </div>
      </label>
</form>  </div>
</div>


      <nav class="d-flex flex-column flex-lg-row flex-self-stretch flex-lg-self-auto" aria-label="Global">
    <a class="Header-link d-block d-lg-none py-2 py-lg-0 border-top border-lg-top-0 border-white-fade-15" data-ga-click="Header, click, Nav menu - item:dashboard:user" aria-label="Dashboard" href="/dashboard">
      Dashboard
</a>
  <a class="js-selected-navigation-item Header-link  mr-0 mr-lg-3 py-2 py-lg-0 border-top border-lg-top-0 border-white-fade-15" data-hotkey="g p" data-ga-click="Header, click, Nav menu - item:pulls context:user" aria-label="Pull requests you created" data-selected-links="/pulls /pulls/assigned /pulls/mentioned /pulls" href="/pulls">
    Pull requests
</a>
  <a class="js-selected-navigation-item Header-link  mr-0 mr-lg-3 py-2 py-lg-0 border-top border-lg-top-0 border-white-fade-15" data-hotkey="g i" data-ga-click="Header, click, Nav menu - item:issues context:user" aria-label="Issues you created" data-selected-links="/issues /issues/assigned /issues/mentioned /issues" href="/issues">
    Issues
</a>
    <a class="js-selected-navigation-item Header-link  mr-0 mr-lg-3 py-2 py-lg-0 border-top border-lg-top-0 border-white-fade-15" data-ga-click="Header, click, Nav menu - item:marketplace context:user" data-octo-click="marketplace_click" data-octo-dimensions="location:nav_bar" data-selected-links=" /marketplace" href="/marketplace">
      Marketplace
</a>      

  <a class="js-selected-navigation-item Header-link  mr-0 mr-lg-3 py-2 py-lg-0 border-top border-lg-top-0 border-white-fade-15" data-ga-click="Header, click, Nav menu - item:explore" data-selected-links="/explore /trending /trending/developers /integrations /integrations/feature/code /integrations/feature/collaborate /integrations/feature/ship showcases showcases_search showcases_landing /explore" href="/explore">
    Explore
</a>
    <a class="Header-link d-block d-lg-none mr-0 mr-lg-3 py-2 py-lg-0 border-top border-lg-top-0 border-white-fade-15" aria-label="View profile and more" aria-expanded="false" aria-haspopup="false" href="https://github.com/moltaweb">
      <img class="avatar" src="https://avatars0.githubusercontent.com/u/20514020?s=40&amp;v=4" width="20" height="20" alt="@moltaweb" />
      moltaweb
</a>
    <!-- '"` --><!-- </textarea></xmp> --></option></form><form action="/logout" accept-charset="UTF-8" method="post"><input name="utf8" type="hidden" value="&#x2713;" /><input type="hidden" name="authenticity_token" value="KhjrPB6GmG4roaIczLDo877D77Tmd9l6P7FUhf7tjH3/PmJd1fgnoOj4CAKf5taUH5m2ke/kek/H7Z+aBPj7Cw==" />
      <button type="submit" class="Header-link mr-0 mr-lg-3 py-2 py-lg-0 border-top border-lg-top-0 border-white-fade-15 d-lg-none btn-link d-block width-full text-left" data-ga-click="Header, sign out, icon:logout" style="padding-left: 2px;">
        <svg class="octicon octicon-sign-out v-align-middle" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M12 9V7H8V5h4V3l4 3-4 3zm-2 3H6V3L2 1h8v3h1V1c0-.55-.45-1-1-1H1C.45 0 0 .45 0 1v11.38c0 .39.22.73.55.91L6 16.01V13h4c.55 0 1-.45 1-1V8h-1v4z"/></svg>
        Sign out
      </button>
</form></nav>

    </div>

    <div class="Header-item Header-item--full flex-justify-center d-lg-none position-relative">
      <div class="css-truncate css-truncate-target width-fit position-absolute left-0 right-0 text-center">
              <svg class="octicon octicon-lock" viewBox="0 0 12 16" version="1.1" width="12" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 13H3v-1h1v1zm8-6v7c0 .55-.45 1-1 1H1c-.55 0-1-.45-1-1V7c0-.55.45-1 1-1h1V4c0-2.2 1.8-4 4-4s4 1.8 4 4v2h1c.55 0 1 .45 1 1zM3.8 6h4.41V4c0-1.22-.98-2.2-2.2-2.2-1.22 0-2.2.98-2.2 2.2v2H3.8zM11 7H2v7h9V7zM4 8H3v1h1V8zm0 2H3v1h1v-1z"/></svg>
    <a class="Header-link" href="/moltaweb">moltaweb</a>
    /
    <a class="Header-link" href="/moltaweb/cursos">cursos</a>

</div>
    </div>

    <div class="Header-item position-relative d-none d-lg-flex">
      

    </div>

    <div class="Header-item mr-0 mr-lg-3 flex-order-1 flex-lg-order-none">
      
    <a aria-label="You have no unread notifications" class="Header-link notification-indicator tooltipped tooltipped-s my-2 my-lg-0 js-socket-channel js-notification-indicator" data-hotkey="g n" data-ga-click="Header, go to notifications, icon:read" data-channel="notification-changed:20514020" href="/notifications">
        <span class="mail-status "></span>
        <svg class="octicon octicon-bell" viewBox="0 0 14 16" version="1.1" width="14" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M14 12v1H0v-1l.73-.58c.77-.77.81-2.55 1.19-4.42C2.69 3.23 6 2 6 2c0-.55.45-1 1-1s1 .45 1 1c0 0 3.39 1.23 4.16 5 .38 1.88.42 3.66 1.19 4.42l.66.58H14zm-7 4c1.11 0 2-.89 2-2H5c0 1.11.89 2 2 2z"/></svg>
</a>
    </div>


    <div class="Header-item position-relative d-none d-lg-flex">
      <details class="details-overlay details-reset">
  <summary class="Header-link"
      aria-label="Create new…"
      data-ga-click="Header, create new, icon:add">
    <svg class="octicon octicon-plus" viewBox="0 0 12 16" version="1.1" width="12" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M12 9H7v5H5V9H0V7h5V2h2v5h5v2z"/></svg> <span class="dropdown-caret"></span>
  </summary>
  <details-menu class="dropdown-menu dropdown-menu-sw">
    
<a role="menuitem" class="dropdown-item" href="/new" data-ga-click="Header, create new repository">
  New repository
</a>

  <a role="menuitem" class="dropdown-item" href="/new/import" data-ga-click="Header, import a repository">
    Import repository
  </a>

<a role="menuitem" class="dropdown-item" href="https://gist.github.com/" data-ga-click="Header, create new gist">
  New gist
</a>

  <a role="menuitem" class="dropdown-item" href="/organizations/new" data-ga-click="Header, create new organization">
    New organization
  </a>


  <div role="none" class="dropdown-divider"></div>
  <div class="dropdown-header">
    <span title="moltaweb/cursos">This repository</span>
  </div>
    <a role="menuitem" class="dropdown-item" href="/moltaweb/cursos/issues/new" data-ga-click="Header, create new issue" data-skip-pjax>
      New issue
    </a>


  </details-menu>
</details>

    </div>

    <div class="Header-item position-relative mr-0 d-none d-lg-flex">
      
<details class="details-overlay details-reset">
  <summary class="Header-link"
    aria-label="View profile and more"
    data-ga-click="Header, show menu, icon:avatar">
    <img alt="@moltaweb" class="avatar" src="https://avatars0.githubusercontent.com/u/20514020?s=40&amp;v=4" height="20" width="20">
    <span class="dropdown-caret"></span>
  </summary>
  <details-menu class="dropdown-menu dropdown-menu-sw mt-2" style="width: 180px">
    <div class="header-nav-current-user css-truncate"><a role="menuitem" class="no-underline user-profile-link px-3 pt-2 pb-2 mb-n2 mt-n1 d-block" href="/moltaweb" data-ga-click="Header, go to profile, text:Signed in as">Signed in as <strong class="css-truncate-target">moltaweb</strong></a></div>
    <div role="none" class="dropdown-divider"></div>

      <div class="pl-3 pr-5 f6 user-status-container js-user-status-context pb-1" data-url="/users/status?compact=1&amp;link_mentions=0&amp;truncate=1">
        
<div class="js-user-status-container  user-status-compact rounded-1 px-2 py-1 mt-2 border" data-team-hovercards-enabled>
  <details class="js-user-status-details details-reset details-overlay details-overlay-dark">
    <summary class="btn-link no-underline js-toggle-user-status-edit toggle-user-status-edit width-full d-flex link-gray " aria-haspopup="dialog" role="menuitem" data-hydro-click="{&quot;event_type&quot;:&quot;user_profile.click&quot;,&quot;payload&quot;:{&quot;profile_user_id&quot;:20514020,&quot;target&quot;:&quot;EDIT_USER_STATUS&quot;,&quot;user_id&quot;:20514020,&quot;client_id&quot;:&quot;850522653.1548880191&quot;,&quot;originating_request_id&quot;:&quot;8F1E:38C41:A43FA3:F7AD76:5CC06BEB&quot;,&quot;originating_url&quot;:&quot;https://github.com/moltaweb/cursos/blob/master/udemy-spring-mvc-chaddarby.md&quot;,&quot;referrer&quot;:&quot;https://github.com/moltaweb/cursos&quot;}}" data-hydro-click-hmac="b216c0c01799f55f63bd7978674cd9c37a818f1aa9c3f7a999a7104e6718593c">
      <div class="f6 d-inline-block v-align-middle user-status-emoji-only-header circle pr-2 lh-condensed user-status-header " style="max-width: 29px">
        <div class="user-status-emoji-container flex-shrink-0 mr-1 mt-1 lh-condensed-ultra v-align-bottom" style="">
          <svg class="octicon octicon-smiley" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M8 0C3.58 0 0 3.58 0 8s3.58 8 8 8 8-3.58 8-8-3.58-8-8-8zm4.81 12.81a6.72 6.72 0 0 1-2.17 1.45c-.83.36-1.72.53-2.64.53-.92 0-1.81-.17-2.64-.53-.81-.34-1.55-.83-2.17-1.45a6.773 6.773 0 0 1-1.45-2.17A6.59 6.59 0 0 1 1.21 8c0-.92.17-1.81.53-2.64.34-.81.83-1.55 1.45-2.17.62-.62 1.36-1.11 2.17-1.45A6.59 6.59 0 0 1 8 1.21c.92 0 1.81.17 2.64.53.81.34 1.55.83 2.17 1.45.62.62 1.11 1.36 1.45 2.17.36.83.53 1.72.53 2.64 0 .92-.17 1.81-.53 2.64-.34.81-.83 1.55-1.45 2.17zM4 6.8v-.59c0-.66.53-1.19 1.2-1.19h.59c.66 0 1.19.53 1.19 1.19v.59c0 .67-.53 1.2-1.19 1.2H5.2C4.53 8 4 7.47 4 6.8zm5 0v-.59c0-.66.53-1.19 1.2-1.19h.59c.66 0 1.19.53 1.19 1.19v.59c0 .67-.53 1.2-1.19 1.2h-.59C9.53 8 9 7.47 9 6.8zm4 3.2c-.72 1.88-2.91 3-5 3s-4.28-1.13-5-3c-.14-.39.23-1 .66-1h8.59c.41 0 .89.61.75 1z"/></svg>
        </div>
      </div>
      <div class="
        d-inline-block v-align-middle
        
        
         css-truncate css-truncate-target 
         user-status-message-wrapper f6"
        style="line-height: 20px;">
        <div class="d-inline-block text-gray-dark v-align-text-top">
            <span class="text-gray ml-2">Set status</span>
        </div>
      </div>
</summary>    <details-dialog class="details-dialog rounded-1 anim-fade-in fast Box Box--overlay" role="dialog" tabindex="-1">
      <!-- '"` --><!-- </textarea></xmp> --></option></form><form class="position-relative flex-auto js-user-status-form" action="/users/status?compact=1&amp;link_mentions=0&amp;truncate=1" accept-charset="UTF-8" method="post"><input name="utf8" type="hidden" value="&#x2713;" /><input type="hidden" name="_method" value="put" /><input type="hidden" name="authenticity_token" value="S32zHfAedERAuAXi3StAhdKpLbWhXj76/I38qgAwGEp3LgLGyonIlhpxPiz8UfomPvgEs4N25kGOtcmJYoAEBw==" />
        <div class="Box-header bg-gray border-bottom p-3">
          <button class="Box-btn-octicon js-toggle-user-status-edit btn-octicon float-right" type="reset" aria-label="Close dialog" data-close-dialog>
            <svg class="octicon octicon-x" viewBox="0 0 12 16" version="1.1" width="12" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.48 8l3.75 3.75-1.48 1.48L6 9.48l-3.75 3.75-1.48-1.48L4.52 8 .77 4.25l1.48-1.48L6 6.52l3.75-3.75 1.48 1.48L7.48 8z"/></svg>
          </button>
          <h3 class="Box-title f5 text-bold text-gray-dark">Edit status</h3>
        </div>
        <input type="hidden" name="emoji" class="js-user-status-emoji-field" value="">
        <input type="hidden" name="organization_id" class="js-user-status-org-id-field" value="">
        <div class="px-3 py-2 text-gray-dark">
          <div class="js-characters-remaining-container js-suggester-container position-relative mt-2">
            <div class="input-group d-table form-group my-0 js-user-status-form-group">
              <span class="input-group-button d-table-cell v-align-middle" style="width: 1%">
                <button type="button" aria-label="Choose an emoji" class="btn-outline btn js-toggle-user-status-emoji-picker btn-open-emoji-picker p-0">
                  <span class="js-user-status-original-emoji" hidden></span>
                  <span class="js-user-status-custom-emoji"></span>
                  <span class="js-user-status-no-emoji-icon" >
                    <svg class="octicon octicon-smiley" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M8 0C3.58 0 0 3.58 0 8s3.58 8 8 8 8-3.58 8-8-3.58-8-8-8zm4.81 12.81a6.72 6.72 0 0 1-2.17 1.45c-.83.36-1.72.53-2.64.53-.92 0-1.81-.17-2.64-.53-.81-.34-1.55-.83-2.17-1.45a6.773 6.773 0 0 1-1.45-2.17A6.59 6.59 0 0 1 1.21 8c0-.92.17-1.81.53-2.64.34-.81.83-1.55 1.45-2.17.62-.62 1.36-1.11 2.17-1.45A6.59 6.59 0 0 1 8 1.21c.92 0 1.81.17 2.64.53.81.34 1.55.83 2.17 1.45.62.62 1.11 1.36 1.45 2.17.36.83.53 1.72.53 2.64 0 .92-.17 1.81-.53 2.64-.34.81-.83 1.55-1.45 2.17zM4 6.8v-.59c0-.66.53-1.19 1.2-1.19h.59c.66 0 1.19.53 1.19 1.19v.59c0 .67-.53 1.2-1.19 1.2H5.2C4.53 8 4 7.47 4 6.8zm5 0v-.59c0-.66.53-1.19 1.2-1.19h.59c.66 0 1.19.53 1.19 1.19v.59c0 .67-.53 1.2-1.19 1.2h-.59C9.53 8 9 7.47 9 6.8zm4 3.2c-.72 1.88-2.91 3-5 3s-4.28-1.13-5-3c-.14-.39.23-1 .66-1h8.59c.41 0 .89.61.75 1z"/></svg>
                  </span>
                </button>
              </span>
              <input type="text" autocomplete="off" data-maxlength="80" class="js-suggester-field d-table-cell width-full form-control js-user-status-message-field js-characters-remaining-field" placeholder="What's happening?" name="message" value="" aria-label="What is your current status?">
              <div class="error">Could not update your status, please try again.</div>
            </div>
            <div class="suggester-container">
              <div class="suggester js-suggester js-navigation-container" data-url="/autocomplete/user-suggestions" data-no-org-url="/autocomplete/user-suggestions" data-org-url="/suggestions" hidden>
              </div>
            </div>
            <div style="margin-left: 53px" class="my-1 text-small label-characters-remaining js-characters-remaining" data-suffix="remaining" hidden>
              80 remaining
            </div>
          </div>
          <include-fragment class="js-user-status-emoji-picker" data-url="/users/status/emoji"></include-fragment>
          <div class="overflow-auto ml-n3 mr-n3 px-3" style="max-height: 33vh">
            <div class="user-status-suggestions js-user-status-suggestions collapsed overflow-hidden">
              <h4 class="f6 text-normal my-3">Suggestions:</h4>
              <div class="mx-3 mt-2 clearfix">
                  <div class="float-left col-6">
                      <button type="button" value=":palm_tree:" class="d-flex flex-items-baseline flex-items-stretch lh-condensed f6 btn-link link-gray no-underline js-predefined-user-status mb-1">
                        <div class="emoji-status-width mr-2 v-align-middle js-predefined-user-status-emoji">
                          <g-emoji alias="palm_tree" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/1f334.png">🌴</g-emoji>
                        </div>
                        <div class="d-flex flex-items-center no-underline js-predefined-user-status-message ws-normal text-left" style="border-left: 1px solid transparent">
                          On vacation
                        </div>
                      </button>
                      <button type="button" value=":face_with_thermometer:" class="d-flex flex-items-baseline flex-items-stretch lh-condensed f6 btn-link link-gray no-underline js-predefined-user-status mb-1">
                        <div class="emoji-status-width mr-2 v-align-middle js-predefined-user-status-emoji">
                          <g-emoji alias="face_with_thermometer" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/1f912.png">🤒</g-emoji>
                        </div>
                        <div class="d-flex flex-items-center no-underline js-predefined-user-status-message ws-normal text-left" style="border-left: 1px solid transparent">
                          Out sick
                        </div>
                      </button>
                  </div>
                  <div class="float-left col-6">
                      <button type="button" value=":house:" class="d-flex flex-items-baseline flex-items-stretch lh-condensed f6 btn-link link-gray no-underline js-predefined-user-status mb-1">
                        <div class="emoji-status-width mr-2 v-align-middle js-predefined-user-status-emoji">
                          <g-emoji alias="house" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/1f3e0.png">🏠</g-emoji>
                        </div>
                        <div class="d-flex flex-items-center no-underline js-predefined-user-status-message ws-normal text-left" style="border-left: 1px solid transparent">
                          Working from home
                        </div>
                      </button>
                      <button type="button" value=":dart:" class="d-flex flex-items-baseline flex-items-stretch lh-condensed f6 btn-link link-gray no-underline js-predefined-user-status mb-1">
                        <div class="emoji-status-width mr-2 v-align-middle js-predefined-user-status-emoji">
                          <g-emoji alias="dart" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/1f3af.png">🎯</g-emoji>
                        </div>
                        <div class="d-flex flex-items-center no-underline js-predefined-user-status-message ws-normal text-left" style="border-left: 1px solid transparent">
                          Focusing
                        </div>
                      </button>
                  </div>
              </div>
            </div>
            <div class="user-status-limited-availability-container">
              <div class="form-checkbox my-0">
                <input type="checkbox" name="limited_availability" value="1" class="js-user-status-limited-availability-checkbox" data-default-message="I may be slow to respond." aria-describedby="limited-availability-help-text-truncate-true" id="limited-availability-truncate-true">
                <label class="d-block f5 text-gray-dark mb-1" for="limited-availability-truncate-true">
                  Busy
                </label>
                <p class="note" id="limited-availability-help-text-truncate-true">
                  When others mention you, assign you, or request your review,
                  GitHub will let them know that you have limited availability.
                </p>
              </div>
            </div>
          </div>
            

<div class="d-inline-block f5 border-top mr-2 pt-3 pb-2" >
  <div class="d-inline-block mr-1">
    Clear status
  </div>

  <details class="js-user-status-expire-drop-down f6 dropdown details-reset details-overlay d-inline-block mr-2">
    <summary class="f5 btn-link link-gray-dark border px-2 py-1 rounded-1" aria-haspopup="true">
      <div class="js-user-status-expiration-interval-selected d-inline-block v-align-baseline">
        Never
      </div>
      <div class="dropdown-caret"></div>
    </summary>

    <ul class="dropdown-menu dropdown-menu-se pl-0 overflow-auto" style="width: 220px; max-height: 15.5em">
      <li>
        <button type="button" class="btn-link dropdown-item js-user-status-expire-button ws-normal" title="Never">
          <span class="d-inline-block text-bold mb-1">Never</span>
          <div class="f6 lh-condensed">Keep this status until you clear your status or edit your status.</div>
        </button>
      </li>
      <li class="dropdown-divider" role="none"></li>
        <li>
          <button type="button" class="btn-link dropdown-item ws-normal js-user-status-expire-button" title="in 30 minutes" value="2019-04-24T16:30:16+02:00">
            in 30 minutes
          </button>
        </li>
        <li>
          <button type="button" class="btn-link dropdown-item ws-normal js-user-status-expire-button" title="in 1 hour" value="2019-04-24T17:00:16+02:00">
            in 1 hour
          </button>
        </li>
        <li>
          <button type="button" class="btn-link dropdown-item ws-normal js-user-status-expire-button" title="in 4 hours" value="2019-04-24T20:00:16+02:00">
            in 4 hours
          </button>
        </li>
        <li>
          <button type="button" class="btn-link dropdown-item ws-normal js-user-status-expire-button" title="today" value="2019-04-24T23:59:59+02:00">
            today
          </button>
        </li>
        <li>
          <button type="button" class="btn-link dropdown-item ws-normal js-user-status-expire-button" title="this week" value="2019-04-28T23:59:59+02:00">
            this week
          </button>
        </li>
    </ul>
  </details>
  <input class="js-user-status-expiration-date-input" type="hidden" name="expires_at" value="">
</div>

          <include-fragment class="js-user-status-org-picker" data-url="/users/status/organizations"></include-fragment>
        </div>
        <div class="d-flex flex-items-center flex-justify-between p-3 border-top">
          <button type="submit" disabled class="width-full btn btn-primary mr-2 js-user-status-submit">
            Set status
          </button>
          <button type="button" disabled class="width-full js-clear-user-status-button btn ml-2 ">
            Clear status
          </button>
        </div>
</form>    </details-dialog>
  </details>
</div>

      </div>
      <div role="none" class="dropdown-divider"></div>


    <a role="menuitem" class="dropdown-item" href="/moltaweb" data-ga-click="Header, go to profile, text:your profile">Your profile</a>
    <a role="menuitem" class="dropdown-item" href="/moltaweb?tab=repositories" data-ga-click="Header, go to repositories, text:your repositories">Your repositories</a>

    <a role="menuitem" class="dropdown-item" href="/moltaweb?tab=projects" data-ga-click="Header, go to projects, text:your projects">Your projects</a>

    <a role="menuitem" class="dropdown-item" href="/moltaweb?tab=stars" data-ga-click="Header, go to starred repos, text:your stars">Your stars</a>
      <a role="menuitem" class="dropdown-item" href="https://gist.github.com/" data-ga-click="Header, your gists, text:your gists">Your gists</a>

    <div role="none" class="dropdown-divider"></div>
    <a role="menuitem" class="dropdown-item" href="https://help.github.com" data-ga-click="Header, go to help, text:help">Help</a>
    <a role="menuitem" class="dropdown-item" href="/settings/profile" data-ga-click="Header, go to settings, icon:settings">Settings</a>
    <!-- '"` --><!-- </textarea></xmp> --></option></form><form class="logout-form" action="/logout" accept-charset="UTF-8" method="post"><input name="utf8" type="hidden" value="&#x2713;" /><input type="hidden" name="authenticity_token" value="hjuJNb6PaJbPYFa+LayrASsoEcSarhz7Q7oIy/EYf7ZTHQBUdfHXWAw5/KB++pVminJI4ZM9v8675sPUCw0IwA==" />
      
      <button type="submit" class="dropdown-item dropdown-signout" data-ga-click="Header, sign out, icon:logout" role="menuitem">
        Sign out
      </button>
</form>  </details-menu>
</details>

    </div>

  </header>

      

  </div>

  <div id="start-of-content" class="show-on-focus"></div>


    <div id="js-flash-container">

</div>



  <div class="application-main " data-commit-hovercards-enabled>
        <div itemscope itemtype="http://schema.org/SoftwareSourceCode" class="">
    <main  >
      


  






  <div class="pagehead repohead instapaper_ignore readability-menu experiment-repo-nav pt-0 pt-lg-4 ">
    <div class="repohead-details-container clearfix container-lg p-responsive d-none d-lg-block">

      <ul class="pagehead-actions">



  <li>
    
    <!-- '"` --><!-- </textarea></xmp> --></option></form><form data-remote="true" class="clearfix js-social-form js-social-container" action="/notifications/subscribe" accept-charset="UTF-8" method="post"><input name="utf8" type="hidden" value="&#x2713;" /><input type="hidden" name="authenticity_token" value="FJDqMFvdKJa8TcGajbGCaW8HjL4VdJRE+aFfiJQhIPOFaF5pWuRRaaKiLMSfVakNVBFCaL27dFmECI95KULmxQ==" />      <input type="hidden" name="repository_id" value="182517889">

      <details class="details-reset details-overlay select-menu float-left">
        <summary class="select-menu-button float-left btn btn-sm btn-with-count" data-hydro-click="{&quot;event_type&quot;:&quot;repository.click&quot;,&quot;payload&quot;:{&quot;target&quot;:&quot;WATCH_BUTTON&quot;,&quot;repository_id&quot;:182517889,&quot;client_id&quot;:&quot;850522653.1548880191&quot;,&quot;originating_request_id&quot;:&quot;8F1E:38C41:A43FA3:F7AD76:5CC06BEB&quot;,&quot;originating_url&quot;:&quot;https://github.com/moltaweb/cursos/blob/master/udemy-spring-mvc-chaddarby.md&quot;,&quot;referrer&quot;:&quot;https://github.com/moltaweb/cursos&quot;,&quot;user_id&quot;:20514020}}" data-hydro-click-hmac="543b4404ec16ae96e8fde5fe4d60971289b6f54f0fbd4d9a98427edce989ed20" data-ga-click="Repository, click Watch settings, action:blob#show">          <span data-menu-button>
              <svg class="octicon octicon-eye v-align-text-bottom" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M8.06 2C3 2 0 8 0 8s3 6 8.06 6C13 14 16 8 16 8s-3-6-7.94-6zM8 12c-2.2 0-4-1.78-4-4 0-2.2 1.8-4 4-4 2.22 0 4 1.8 4 4 0 2.22-1.78 4-4 4zm2-4c0 1.11-.89 2-2 2-1.11 0-2-.89-2-2 0-1.11.89-2 2-2 1.11 0 2 .89 2 2z"/></svg>
              Unwatch
          </span>
</summary>        <details-menu
          class="select-menu-modal position-absolute mt-5"
          style="z-index: 99;">
          <div class="select-menu-header">
            <span class="select-menu-title">Notifications</span>
          </div>
          <div class="select-menu-list">
            <button type="submit" name="do" value="included" class="select-menu-item width-full" aria-checked="false" role="menuitemradio">
              <svg class="octicon octicon-check select-menu-item-icon" viewBox="0 0 12 16" version="1.1" width="12" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M12 5l-8 8-4-4 1.5-1.5L4 10l6.5-6.5L12 5z"/></svg>
              <div class="select-menu-item-text">
                <span class="select-menu-item-heading">Not watching</span>
                <span class="description">Be notified only when participating or @mentioned.</span>
                <span class="hidden-select-button-text" data-menu-button-contents>
                  <svg class="octicon octicon-eye v-align-text-bottom" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M8.06 2C3 2 0 8 0 8s3 6 8.06 6C13 14 16 8 16 8s-3-6-7.94-6zM8 12c-2.2 0-4-1.78-4-4 0-2.2 1.8-4 4-4 2.22 0 4 1.8 4 4 0 2.22-1.78 4-4 4zm2-4c0 1.11-.89 2-2 2-1.11 0-2-.89-2-2 0-1.11.89-2 2-2 1.11 0 2 .89 2 2z"/></svg>
                  Watch
                </span>
              </div>
            </button>

            <button type="submit" name="do" value="release_only" class="select-menu-item width-full" aria-checked="false" role="menuitemradio">
              <svg class="octicon octicon-check select-menu-item-icon" viewBox="0 0 12 16" version="1.1" width="12" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M12 5l-8 8-4-4 1.5-1.5L4 10l6.5-6.5L12 5z"/></svg>
              <div class="select-menu-item-text">
                <span class="select-menu-item-heading">Releases only</span>
                <span class="description">Be notified of new releases, and when participating or @mentioned.</span>
                <span class="hidden-select-button-text" data-menu-button-contents>
                  <svg class="octicon octicon-eye v-align-text-bottom" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M8.06 2C3 2 0 8 0 8s3 6 8.06 6C13 14 16 8 16 8s-3-6-7.94-6zM8 12c-2.2 0-4-1.78-4-4 0-2.2 1.8-4 4-4 2.22 0 4 1.8 4 4 0 2.22-1.78 4-4 4zm2-4c0 1.11-.89 2-2 2-1.11 0-2-.89-2-2 0-1.11.89-2 2-2 1.11 0 2 .89 2 2z"/></svg>
                  Unwatch releases
                </span>
              </div>
            </button>

            <button type="submit" name="do" value="subscribed" class="select-menu-item width-full" aria-checked="true" role="menuitemradio">
              <svg class="octicon octicon-check select-menu-item-icon" viewBox="0 0 12 16" version="1.1" width="12" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M12 5l-8 8-4-4 1.5-1.5L4 10l6.5-6.5L12 5z"/></svg>
              <div class="select-menu-item-text">
                <span class="select-menu-item-heading">Watching</span>
                <span class="description">Be notified of all conversations.</span>
                <span class="hidden-select-button-text" data-menu-button-contents>
                  <svg class="octicon octicon-eye v-align-text-bottom" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M8.06 2C3 2 0 8 0 8s3 6 8.06 6C13 14 16 8 16 8s-3-6-7.94-6zM8 12c-2.2 0-4-1.78-4-4 0-2.2 1.8-4 4-4 2.22 0 4 1.8 4 4 0 2.22-1.78 4-4 4zm2-4c0 1.11-.89 2-2 2-1.11 0-2-.89-2-2 0-1.11.89-2 2-2 1.11 0 2 .89 2 2z"/></svg>
                  Unwatch
                </span>
              </div>
            </button>

            <button type="submit" name="do" value="ignore" class="select-menu-item width-full" aria-checked="false" role="menuitemradio">
              <svg class="octicon octicon-check select-menu-item-icon" viewBox="0 0 12 16" version="1.1" width="12" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M12 5l-8 8-4-4 1.5-1.5L4 10l6.5-6.5L12 5z"/></svg>
              <div class="select-menu-item-text">
                <span class="select-menu-item-heading">Ignoring</span>
                <span class="description">Never be notified.</span>
                <span class="hidden-select-button-text" data-menu-button-contents>
                  <svg class="octicon octicon-mute v-align-text-bottom" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M8 2.81v10.38c0 .67-.81 1-1.28.53L3 10H1c-.55 0-1-.45-1-1V7c0-.55.45-1 1-1h2l3.72-3.72C7.19 1.81 8 2.14 8 2.81zm7.53 3.22l-1.06-1.06-1.97 1.97-1.97-1.97-1.06 1.06L11.44 8 9.47 9.97l1.06 1.06 1.97-1.97 1.97 1.97 1.06-1.06L13.56 8l1.97-1.97z"/></svg>
                  Stop ignoring
                </span>
              </div>
            </button>
          </div>
        </details-menu>
      </details>
        <a class="social-count js-social-count"
          href="/moltaweb/cursos/watchers"
          aria-label="1 user is watching this repository">
          1
        </a>
</form>
  </li>

  <li>
      <div class="js-toggler-container js-social-container starring-container ">
    <!-- '"` --><!-- </textarea></xmp> --></option></form><form class="starred js-social-form" action="/moltaweb/cursos/unstar" accept-charset="UTF-8" method="post"><input name="utf8" type="hidden" value="&#x2713;" /><input type="hidden" name="authenticity_token" value="yX0ai2TGxqFae9ysy4BMBa1OgttpSldGmcipzLvsTpJ/4e9vZRwLmjeJeTzZcWPs9nlUU7wT84rovJsIGXHAWg==" />
      <input type="hidden" name="context" value="repository"></input>
      <button type="submit" class="btn btn-sm btn-with-count js-toggler-target" aria-label="Unstar this repository" title="Unstar moltaweb/cursos" data-hydro-click="{&quot;event_type&quot;:&quot;repository.click&quot;,&quot;payload&quot;:{&quot;target&quot;:&quot;UNSTAR_BUTTON&quot;,&quot;repository_id&quot;:182517889,&quot;client_id&quot;:&quot;850522653.1548880191&quot;,&quot;originating_request_id&quot;:&quot;8F1E:38C41:A43FA3:F7AD76:5CC06BEB&quot;,&quot;originating_url&quot;:&quot;https://github.com/moltaweb/cursos/blob/master/udemy-spring-mvc-chaddarby.md&quot;,&quot;referrer&quot;:&quot;https://github.com/moltaweb/cursos&quot;,&quot;user_id&quot;:20514020}}" data-hydro-click-hmac="5e75978bd5f910d3b8a302903d7860ec076d752c91ca221d6fb3c45df9886c7c" data-ga-click="Repository, click unstar button, action:blob#show; text:Unstar">        <svg class="octicon octicon-star v-align-text-bottom" viewBox="0 0 14 16" version="1.1" width="14" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M14 6l-4.9-.64L7 1 4.9 5.36 0 6l3.6 3.26L2.67 14 7 11.67 11.33 14l-.93-4.74L14 6z"/></svg>
        Unstar
</button>        <a class="social-count js-social-count" href="/moltaweb/cursos/stargazers"
           aria-label="0 users starred this repository">
          0
        </a>
</form>
    <!-- '"` --><!-- </textarea></xmp> --></option></form><form class="unstarred js-social-form" action="/moltaweb/cursos/star" accept-charset="UTF-8" method="post"><input name="utf8" type="hidden" value="&#x2713;" /><input type="hidden" name="authenticity_token" value="/gEtuyPw2R9QnCaUSLE6EhMjbN3Unyu6nQOH/Uj3KE0hkPxGStvgGuKH+P0aRXFYtq38Mkwr9FMtLtvdQLSd+w==" />
      <input type="hidden" name="context" value="repository"></input>
      <button type="submit" class="btn btn-sm btn-with-count js-toggler-target" aria-label="Unstar this repository" title="Star moltaweb/cursos" data-hydro-click="{&quot;event_type&quot;:&quot;repository.click&quot;,&quot;payload&quot;:{&quot;target&quot;:&quot;STAR_BUTTON&quot;,&quot;repository_id&quot;:182517889,&quot;client_id&quot;:&quot;850522653.1548880191&quot;,&quot;originating_request_id&quot;:&quot;8F1E:38C41:A43FA3:F7AD76:5CC06BEB&quot;,&quot;originating_url&quot;:&quot;https://github.com/moltaweb/cursos/blob/master/udemy-spring-mvc-chaddarby.md&quot;,&quot;referrer&quot;:&quot;https://github.com/moltaweb/cursos&quot;,&quot;user_id&quot;:20514020}}" data-hydro-click-hmac="db8b44ae01c20914a02375beb72c5546a6caf9ae0cb1575526e65a5660bd3b8f" data-ga-click="Repository, click star button, action:blob#show; text:Star">        <svg class="octicon octicon-star v-align-text-bottom" viewBox="0 0 14 16" version="1.1" width="14" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M14 6l-4.9-.64L7 1 4.9 5.36 0 6l3.6 3.26L2.67 14 7 11.67 11.33 14l-.93-4.74L14 6z"/></svg>
        Star
</button>        <a class="social-count js-social-count" href="/moltaweb/cursos/stargazers"
           aria-label="0 users starred this repository">
          0
        </a>
</form>  </div>

  </li>

  <li>
        <span class="btn btn-sm btn-with-count disabled tooltipped tooltipped-sw" aria-label="Cannot fork because you own this repository and are not a member of any organizations.">
          <svg class="octicon octicon-repo-forked v-align-text-bottom" viewBox="0 0 10 16" version="1.1" width="10" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M8 1a1.993 1.993 0 0 0-1 3.72V6L5 8 3 6V4.72A1.993 1.993 0 0 0 2 1a1.993 1.993 0 0 0-1 3.72V6.5l3 3v1.78A1.993 1.993 0 0 0 5 15a1.993 1.993 0 0 0 1-3.72V9.5l3-3V4.72A1.993 1.993 0 0 0 8 1zM2 4.2C1.34 4.2.8 3.65.8 3c0-.65.55-1.2 1.2-1.2.65 0 1.2.55 1.2 1.2 0 .65-.55 1.2-1.2 1.2zm3 10c-.66 0-1.2-.55-1.2-1.2 0-.65.55-1.2 1.2-1.2.65 0 1.2.55 1.2 1.2 0 .65-.55 1.2-1.2 1.2zm3-10c-.66 0-1.2-.55-1.2-1.2 0-.65.55-1.2 1.2-1.2.65 0 1.2.55 1.2 1.2 0 .65-.55 1.2-1.2 1.2z"/></svg>
          Fork
</span>
    <a href="/moltaweb/cursos/network/members" class="social-count"
       aria-label="0 users forked this repository">
      0
    </a>
  </li>
</ul>

      <h1 class="private ">
  <svg class="octicon octicon-lock" viewBox="0 0 12 16" version="1.1" width="12" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 13H3v-1h1v1zm8-6v7c0 .55-.45 1-1 1H1c-.55 0-1-.45-1-1V7c0-.55.45-1 1-1h1V4c0-2.2 1.8-4 4-4s4 1.8 4 4v2h1c.55 0 1 .45 1 1zM3.8 6h4.41V4c0-1.22-.98-2.2-2.2-2.2-1.22 0-2.2.98-2.2 2.2v2H3.8zM11 7H2v7h9V7zM4 8H3v1h1V8zm0 2H3v1h1v-1z"/></svg>
  <span class="author" itemprop="author"><a class="url fn" rel="author" data-hovercard-type="user" data-hovercard-url="/hovercards?user_id=20514020" data-octo-click="hovercard-link-click" data-octo-dimensions="link_type:self" href="/moltaweb">moltaweb</a></span><!--
--><span class="path-divider">/</span><!--
--><strong itemprop="name"><a data-pjax="#js-repo-pjax-container" href="/moltaweb/cursos">cursos</a></strong>
  <span class="Label Label--outline v-align-middle">Private</span>

</h1>

    </div>
    
<nav class="reponav js-repo-nav js-sidenav-container-pjax container-lg p-responsive d-none d-lg-block"
     itemscope
     itemtype="http://schema.org/BreadcrumbList"
    aria-label="Repository"
     data-pjax="#js-repo-pjax-container">

  <span itemscope itemtype="http://schema.org/ListItem" itemprop="itemListElement">
    <a class="js-selected-navigation-item selected reponav-item" itemprop="url" data-hotkey="g c" aria-current="page" data-selected-links="repo_source repo_downloads repo_commits repo_releases repo_tags repo_branches repo_packages /moltaweb/cursos" href="/moltaweb/cursos">
      <svg class="octicon octicon-code" viewBox="0 0 14 16" version="1.1" width="14" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M9.5 3L8 4.5 11.5 8 8 11.5 9.5 13 14 8 9.5 3zm-5 0L0 8l4.5 5L6 11.5 2.5 8 6 4.5 4.5 3z"/></svg>
      <span itemprop="name">Code</span>
      <meta itemprop="position" content="1">
</a>  </span>

    <span itemscope itemtype="http://schema.org/ListItem" itemprop="itemListElement">
      <a itemprop="url" data-hotkey="g i" class="js-selected-navigation-item reponav-item" data-selected-links="repo_issues repo_labels repo_milestones /moltaweb/cursos/issues" href="/moltaweb/cursos/issues">
        <svg class="octicon octicon-issue-opened" viewBox="0 0 14 16" version="1.1" width="14" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7 2.3c3.14 0 5.7 2.56 5.7 5.7s-2.56 5.7-5.7 5.7A5.71 5.71 0 0 1 1.3 8c0-3.14 2.56-5.7 5.7-5.7zM7 1C3.14 1 0 4.14 0 8s3.14 7 7 7 7-3.14 7-7-3.14-7-7-7zm1 3H6v5h2V4zm0 6H6v2h2v-2z"/></svg>
        <span itemprop="name">Issues</span>
        <span class="Counter">0</span>
        <meta itemprop="position" content="2">
</a>    </span>

  <span itemscope itemtype="http://schema.org/ListItem" itemprop="itemListElement">
    <a data-hotkey="g p" itemprop="url" class="js-selected-navigation-item reponav-item" data-selected-links="repo_pulls checks /moltaweb/cursos/pulls" href="/moltaweb/cursos/pulls">
      <svg class="octicon octicon-git-pull-request" viewBox="0 0 12 16" version="1.1" width="12" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M11 11.28V5c-.03-.78-.34-1.47-.94-2.06C9.46 2.35 8.78 2.03 8 2H7V0L4 3l3 3V4h1c.27.02.48.11.69.31.21.2.3.42.31.69v6.28A1.993 1.993 0 0 0 10 15a1.993 1.993 0 0 0 1-3.72zm-1 2.92c-.66 0-1.2-.55-1.2-1.2 0-.65.55-1.2 1.2-1.2.65 0 1.2.55 1.2 1.2 0 .65-.55 1.2-1.2 1.2zM4 3c0-1.11-.89-2-2-2a1.993 1.993 0 0 0-1 3.72v6.56A1.993 1.993 0 0 0 2 15a1.993 1.993 0 0 0 1-3.72V4.72c.59-.34 1-.98 1-1.72zm-.8 10c0 .66-.55 1.2-1.2 1.2-.65 0-1.2-.55-1.2-1.2 0-.65.55-1.2 1.2-1.2.65 0 1.2.55 1.2 1.2zM2 4.2C1.34 4.2.8 3.65.8 3c0-.65.55-1.2 1.2-1.2.65 0 1.2.55 1.2 1.2 0 .65-.55 1.2-1.2 1.2z"/></svg>
      <span itemprop="name">Pull requests</span>
      <span class="Counter">0</span>
      <meta itemprop="position" content="3">
</a>  </span>



    <a data-hotkey="g b" class="js-selected-navigation-item reponav-item" data-selected-links="repo_projects new_repo_project repo_project /moltaweb/cursos/projects" href="/moltaweb/cursos/projects">
      <svg class="octicon octicon-project" viewBox="0 0 15 16" version="1.1" width="15" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M10 12h3V2h-3v10zm-4-2h3V2H6v8zm-4 4h3V2H2v12zm-1 1h13V1H1v14zM14 0H1a1 1 0 0 0-1 1v14a1 1 0 0 0 1 1h13a1 1 0 0 0 1-1V1a1 1 0 0 0-1-1z"/></svg>
      Projects
      <span class="Counter" >0</span>
</a>


    <a class="js-selected-navigation-item reponav-item" data-selected-links="repo_graphs repo_contributors dependency_graph pulse people alerts /moltaweb/cursos/network/dependencies" href="/moltaweb/cursos/network/dependencies">
      <svg class="octicon octicon-graph" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M16 14v1H0V0h1v14h15zM5 13H3V8h2v5zm4 0H7V3h2v10zm4 0h-2V6h2v7z"/></svg>
      Insights
</a>
    <a class="js-selected-navigation-item reponav-item" data-selected-links="repo_settings repo_branch_settings hooks integration_installations repo_keys_settings issue_template_editor /moltaweb/cursos/settings" href="/moltaweb/cursos/settings">
      <svg class="octicon octicon-gear" viewBox="0 0 14 16" version="1.1" width="14" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M14 8.77v-1.6l-1.94-.64-.45-1.09.88-1.84-1.13-1.13-1.81.91-1.09-.45-.69-1.92h-1.6l-.63 1.94-1.11.45-1.84-.88-1.13 1.13.91 1.81-.45 1.09L0 7.23v1.59l1.94.64.45 1.09-.88 1.84 1.13 1.13 1.81-.91 1.09.45.69 1.92h1.59l.63-1.94 1.11-.45 1.84.88 1.13-1.13-.92-1.81.47-1.09L14 8.75v.02zM7 11c-1.66 0-3-1.34-3-3s1.34-3 3-3 3 1.34 3 3-1.34 3-3 3z"/></svg>
      Settings
</a>
</nav>

  <div class="reponav-wrapper reponav-small d-lg-none">
  <nav class="reponav js-reponav text-center no-wrap"
       itemscope
       itemtype="http://schema.org/BreadcrumbList">

    <span itemscope itemtype="http://schema.org/ListItem" itemprop="itemListElement">
      <a class="js-selected-navigation-item selected reponav-item" itemprop="url" aria-current="page" data-selected-links="repo_source repo_downloads repo_commits repo_releases repo_tags repo_branches repo_packages /moltaweb/cursos" href="/moltaweb/cursos">
        <span itemprop="name">Code</span>
        <meta itemprop="position" content="1">
</a>    </span>

      <span itemscope itemtype="http://schema.org/ListItem" itemprop="itemListElement">
        <a itemprop="url" class="js-selected-navigation-item reponav-item" data-selected-links="repo_issues repo_labels repo_milestones /moltaweb/cursos/issues" href="/moltaweb/cursos/issues">
          <span itemprop="name">Issues</span>
          <span class="Counter">0</span>
          <meta itemprop="position" content="2">
</a>      </span>

    <span itemscope itemtype="http://schema.org/ListItem" itemprop="itemListElement">
      <a itemprop="url" class="js-selected-navigation-item reponav-item" data-selected-links="repo_pulls checks /moltaweb/cursos/pulls" href="/moltaweb/cursos/pulls">
        <span itemprop="name">Pull requests</span>
        <span class="Counter">0</span>
        <meta itemprop="position" content="3">
</a>    </span>


      <span itemscope itemtype="http://schema.org/ListItem" itemprop="itemListElement">
        <a itemprop="url" class="js-selected-navigation-item reponav-item" data-selected-links="repo_projects new_repo_project repo_project /moltaweb/cursos/projects" href="/moltaweb/cursos/projects">
          <span itemprop="name">Projects</span>
          <span class="Counter">0</span>
          <meta itemprop="position" content="5">
</a>      </span>




  </nav>
</div>


  </div>
<div class="container-lg new-discussion-timeline experiment-repo-nav  p-responsive">
  <div class="repository-content ">

    
    



  
    <a class="d-none js-permalink-shortcut" data-hotkey="y" href="/moltaweb/cursos/blob/59641458aed13c7d49a82608979ed104bf794a63/udemy-spring-mvc-chaddarby.md">Permalink</a>

    <!-- blob contrib key: blob_contributors:v21:63a7060ceaea28284a9104c685757901 -->
      

    <div class="d-flex flex-items-start mb-3 flex-column flex-md-row">
      <span class="d-flex flex-justify-between width-full width-md-auto">
        
<details class="details-reset details-overlay select-menu branch-select-menu ">
  <summary class="btn btn-sm select-menu-button css-truncate"
           data-hotkey="w"
           
           title="Switch branches or tags">
    <i>Branch:</i>
    <span class="css-truncate-target">master</span>
  </summary>

  <details-menu class="select-menu-modal position-absolute" style="z-index: 99;" src="/moltaweb/cursos/ref-list/master/udemy-spring-mvc-chaddarby.md?source_action=show&amp;source_controller=blob" preload>
    <include-fragment class="select-menu-loading-overlay anim-pulse">
      <svg height="32" class="octicon octicon-octoface" viewBox="0 0 16 16" version="1.1" width="32" aria-hidden="true"><path fill-rule="evenodd" d="M14.7 5.34c.13-.32.55-1.59-.13-3.31 0 0-1.05-.33-3.44 1.3-1-.28-2.07-.32-3.13-.32s-2.13.04-3.13.32c-2.39-1.64-3.44-1.3-3.44-1.3-.68 1.72-.26 2.99-.13 3.31C.49 6.21 0 7.33 0 8.69 0 13.84 3.33 15 7.98 15S16 13.84 16 8.69c0-1.36-.49-2.48-1.3-3.35zM8 14.02c-3.3 0-5.98-.15-5.98-3.35 0-.76.38-1.48 1.02-2.07 1.07-.98 2.9-.46 4.96-.46 2.07 0 3.88-.52 4.96.46.65.59 1.02 1.3 1.02 2.07 0 3.19-2.68 3.35-5.98 3.35zM5.49 9.01c-.66 0-1.2.8-1.2 1.78s.54 1.79 1.2 1.79c.66 0 1.2-.8 1.2-1.79s-.54-1.78-1.2-1.78zm5.02 0c-.66 0-1.2.79-1.2 1.78s.54 1.79 1.2 1.79c.66 0 1.2-.8 1.2-1.79s-.53-1.78-1.2-1.78z"/></svg>
    </include-fragment>
  </details-menu>
</details>

        <div class="BtnGroup flex-shrink-0 d-md-none">
          <a href="/moltaweb/cursos/find/master"
                class="js-pjax-capture-input btn btn-sm BtnGroup-item"
                data-pjax
                data-hotkey="t">
            Find file
          </a>
          <clipboard-copy value="udemy-spring-mvc-chaddarby.md" class="btn btn-sm BtnGroup-item">
            Copy path
          </clipboard-copy>
        </div>
      </span>
      <h2 id="blob-path" class="breadcrumb flex-auto min-width-0 text-normal flex-md-self-center ml-md-2 mr-md-3 my-2 my-md-0">
        <span class="js-repo-root text-bold"><span class="js-path-segment"><a data-pjax="true" href="/moltaweb/cursos"><span>cursos</span></a></span></span><span class="separator">/</span><strong class="final-path">udemy-spring-mvc-chaddarby.md</strong>
      </h2>

      <div class="BtnGroup flex-shrink-0 d-none d-md-inline-block">
        <a href="/moltaweb/cursos/find/master"
              class="js-pjax-capture-input btn btn-sm BtnGroup-item"
              data-pjax
              data-hotkey="t">
          Find file
        </a>
        <clipboard-copy value="udemy-spring-mvc-chaddarby.md" class="btn btn-sm BtnGroup-item">
          Copy path
        </clipboard-copy>
      </div>
    </div>



    <include-fragment src="/moltaweb/cursos/contributors/master/udemy-spring-mvc-chaddarby.md" class="Box Box--condensed commit-loader">
      <div class="Box-body bg-blue-light f6">
        Fetching contributors&hellip;
      </div>

      <div class="Box-body d-flex flex-items-center" >
          <img alt="" class="loader-loading mr-2" src="https://github.githubassets.com/images/spinners/octocat-spinner-32-EAF2F5.gif" width="16" height="16" />
        <span class="text-red h6 loader-error">Cannot retrieve contributors at this time</span>
      </div>
</include-fragment>




    <div class="Box mt-3 position-relative">
      
<div class="Box-header py-2 d-flex flex-column flex-shrink-0 flex-md-row flex-md-items-center">

  <div class="text-mono f6 flex-auto pr-3 flex-order-2 flex-md-order-1 mt-2 mt-md-0">
      1095 lines (707 sloc)
      <span class="file-info-divider"></span>
    31.6 KB
  </div>

  <div class="d-flex py-1 py-md-0 flex-auto flex-order-1 flex-md-order-2 flex-sm-grow-0 flex-justify-between">

    <div class="BtnGroup">
      <a id="raw-url" class="btn btn-sm BtnGroup-item" href="/moltaweb/cursos/raw/master/udemy-spring-mvc-chaddarby.md">Raw</a>
        <a class="btn btn-sm js-update-url-with-hash BtnGroup-item" data-hotkey="b" href="/moltaweb/cursos/blame/master/udemy-spring-mvc-chaddarby.md">Blame</a>
      <a rel="nofollow" class="btn btn-sm BtnGroup-item" href="/moltaweb/cursos/commits/master/udemy-spring-mvc-chaddarby.md">History</a>
    </div>


    <div>

            <!-- '"` --><!-- </textarea></xmp> --></option></form><form class="inline-form js-update-url-with-hash" action="/moltaweb/cursos/edit/master/udemy-spring-mvc-chaddarby.md" accept-charset="UTF-8" method="post"><input name="utf8" type="hidden" value="&#x2713;" /><input type="hidden" name="authenticity_token" value="e44nYoRjXC7yP+hJs/YMfjWyXQ888I22Mb0fxbJ4WnNb1TZ6H/83Ro+IMVMVgMubZF6qPf6PZE3o7zRR8vAdXg==" />
              <button class="btn-octicon tooltipped tooltipped-nw" type="submit"
                aria-label="Edit this file" data-hotkey="e" data-disable-with>
                <svg class="octicon octicon-pencil" viewBox="0 0 14 16" version="1.1" width="14" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M0 12v3h3l8-8-3-3-8 8zm3 2H1v-2h1v1h1v1zm10.3-9.3L12 6 9 3l1.3-1.3a.996.996 0 0 1 1.41 0l1.59 1.59c.39.39.39 1.02 0 1.41z"/></svg>
              </button>
</form>
          <!-- '"` --><!-- </textarea></xmp> --></option></form><form class="inline-form" action="/moltaweb/cursos/delete/master/udemy-spring-mvc-chaddarby.md" accept-charset="UTF-8" method="post"><input name="utf8" type="hidden" value="&#x2713;" /><input type="hidden" name="authenticity_token" value="dK9iNm6Ak+3ERXyAEW0d9D0/I0I4V+fPY9OQqObxy+NLX2kIPM3CRrsqvJ10Np9FAg7ANmANbCca3cgjwuZfVQ==" />
            <button class="btn-octicon btn-octicon-danger tooltipped tooltipped-nw" type="submit"
              aria-label="Delete this file" data-disable-with>
              <svg class="octicon octicon-trashcan" viewBox="0 0 12 16" version="1.1" width="12" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M11 2H9c0-.55-.45-1-1-1H5c-.55 0-1 .45-1 1H2c-.55 0-1 .45-1 1v1c0 .55.45 1 1 1v9c0 .55.45 1 1 1h7c.55 0 1-.45 1-1V5c.55 0 1-.45 1-1V3c0-.55-.45-1-1-1zm-1 12H3V5h1v8h1V5h1v8h1V5h1v8h1V5h1v9zm1-10H2V3h9v1z"/></svg>
            </button>
</form>    </div>
  </div>
</div>

      
  <div id="readme" class="Box-body readme blob instapaper_body js-code-block-container">
    <article class="markdown-body entry-content p-3 p-md-6" itemprop="text"><p>questions</p>
<ul>
<li>what if no @override? it also works the same, so what's the advatnage</li>
<li>Coach theCoach = context.getBean("mycoach", Coach.class); - por que le pasamos los 2? con el id no es suficiente?</li>
<li>method 2 annotations: what'se the point? its in the middle with both disadvantages</li>
<li>method 3: scope and lifecycle?</li>
<li>148: why the validation is displayes in processFor</li>
</ul>
<hr>
<h2><a id="user-content-course-introduction" class="anchor" aria-hidden="true" href="#course-introduction"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>COURSE INTRODUCTION</h2>
<h3><a id="user-content-introduction" class="anchor" aria-hidden="true" href="#introduction"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Introduction</h3>
<p>Spring and Hibernate are very demanded skills for Java developers</p>
<h3><a id="user-content-practice-activities" class="anchor" aria-hidden="true" href="#practice-activities"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Practice Activities</h3>
<p>It is highly recommended to do all the practice activities and homework on our own. This is the best way to learn</p>
<h3><a id="user-content-how-to-take-this-course" class="anchor" aria-hidden="true" href="#how-to-take-this-course"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>How to take this course</h3>
<p>Some students will watch the video first and then replay it while typing in the code. Others like to type along on the first watch. Choose whatever approach works for you.</p>
<h3><a id="user-content-downloading-source-code-and-pdf-files" class="anchor" aria-hidden="true" href="#downloading-source-code-and-pdf-files"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Downloading source code and PDF files</h3>
<p><strong>Download Source Code:</strong></p>
<p>This only includes the source files, no JAR files. You will need to add JAR files separately on your own.</p>
<p><a href="http://www.luv2code.com/downloads/udemy-spring-hibernate/spring-hibernate-source-code-v26.zip" rel="nofollow">http://www.luv2code.com/downloads/udemy-spring-hibernate/spring-hibernate-source-code-v26.zip</a></p>
<p><strong>Download PDF Files</strong></p>
<p>All slides which are shown during the course are available also as a reference and can be downloaded here:</p>
<p><a href="http://www.luv2code.com/download-spring-hibernate-pdfs" rel="nofollow">http://www.luv2code.com/download-spring-hibernate-pdfs</a></p>
<hr>
<h2><a id="user-content-spring-overview" class="anchor" aria-hidden="true" href="#spring-overview"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>SPRING OVERVIEW</h2>
<hr>
<h2><a id="user-content-setting-up-your-development-environment" class="anchor" aria-hidden="true" href="#setting-up-your-development-environment"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>SETTING UP YOUR DEVELOPMENT ENVIRONMENT</h2>
<h3><a id="user-content-downloading-spring-5-jar-files---installation" class="anchor" aria-hidden="true" href="#downloading-spring-5-jar-files---installation"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Downloading Spring 5 JAR files - Installation</h3>
<ol>
<li>Select latest version of Spring at <a href="https://repo.spring.io/release/org/springframework/spring/" rel="nofollow">https://repo.spring.io/release/org/springframework/spring/</a></li>
<li>Download the "dist" file</li>
<li>Open New Java Project (plain Java) in Eclipse</li>
<li>Create new folder "lib"</li>
<li>In the downloaded zip, copy all the jar files in the "lib" folder</li>
<li>Paste in "lib" in Eclipse</li>
<li>Right click on the project &gt; Properties &gt; Java Build Path &gt; Libraries</li>
<li>Add JARs and select (CTRL SHIFT) all the jar files in lib</li>
<li>Ok. Now they are added to the project runtime</li>
</ol>
<hr>
<h2><a id="user-content-spring-inversion-of-control---xml-configuration" class="anchor" aria-hidden="true" href="#spring-inversion-of-control---xml-configuration"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>SPRING INVERSION OF CONTROL - XML CONFIGURATION</h2>
<h3><a id="user-content-what-is-inversion-of-control" class="anchor" aria-hidden="true" href="#what-is-inversion-of-control"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>What is Inversion of Control?</h3>
<p>IoC is the buzzword we always hear when we talk about Spring.<br>
It's simply the design process of externalizing the construction and management of our objects. The creation of objects will be outsourced to an object factory.</p>
<p>It's passing an XML config file where we define the beans (objects that the factory container instantiates at runtime)</p>
<h3><a id="user-content-code-demo" class="anchor" aria-hidden="true" href="#code-demo"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Code Demo</h3>
<p>We'll see an example through code: BaseBall coach + other sports</p>
<p>Requirement:</p>
<ul>
<li>handle different types of coaches/sports</li>
<li>app should be configurable</li>
</ul>
<p>To make it configurable, it would be great if we had a simple config file that we could use rather than hard code the object implementations</p>
<h3><a id="user-content-spring-ioc---overview" class="anchor" aria-hidden="true" href="#spring-ioc---overview"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Spring IoC - Overview</h3>
<p>Primary functions of Spring framework</p>
<ul>
<li>Create and manage objects (Inversion of Control)</li>
<li>Inject object's dependencies (Dependency Injection)</li>
</ul>
<p>There are 3 ways of configuring the Spring container:</p>
<ol>
<li>XML configuration file (legacy, but most legacy apps still use this)</li>
<li>Java Annotations (modern)</li>
<li>Java Code (modern)</li>
</ol>
<p>Spring Development Process</p>
<ol>
<li>configure Spring Beans</li>
<li>create a Spring container (known as ApplicationContext)</li>
<li>retrieve Beans from Spring container</li>
</ol>
<hr>
<h2><a id="user-content-5---spring-dependency-injection---xml-configuration" class="anchor" aria-hidden="true" href="#5---spring-dependency-injection---xml-configuration"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>5 - SPRING DEPENDENCY INJECTION - XML CONFIGURATION</h2>
<h3><a id="user-content-spring-di---overview" class="anchor" aria-hidden="true" href="#spring-di---overview"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Spring DI - Overview</h3>
<p>There are many types of injection in Spring. The 2 most common:</p>
<ul>
<li>Constructor Injection</li>
<li>Setter Injection</li>
</ul>
<blockquote>
<p>injection = helper</p>
</blockquote>
<p>Injection it's just the fact that when we do a getBean(), we get it with all its dependent objects already instantiated (we will talk about autowiring in the annotations section later)</p>
<p><strong>Constructor injection. steps:</strong></p>
<ol>
<li>define the dependency interface and class</li>
<li>create a constructor in your class that accepts the injections</li>
<li>configure the DI in the Spring config file <code>&lt;constructor-arg&gt;</code></li>
</ol>
<h3><a id="user-content-setter-injection---overview" class="anchor" aria-hidden="true" href="#setter-injection---overview"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Setter Injection - Overview</h3>
<p>Spring will inject dependencies by calling setter methods from our classes</p>
<p>Steps</p>
<ol>
<li>create setter methods in our class for injections</li>
<li>configure the DI in Spring config file <code>&lt;property name&gt;</code></li>
</ol>
<p><code>&lt;property name="nameOfTheProperty"&gt;</code><br>
it expects to find a setter: <code>setNameOfTheProperty()</code></p>
<h3><a id="user-content-setter-injection---injecting-literal-values" class="anchor" aria-hidden="true" href="#setter-injection---injecting-literal-values"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Setter Injection - Injecting literal values</h3>
<p>We can also inject literal values in the XML<br>
<code>&lt;property name="emailAddress" value="hello@me.com"&gt;</code></p>
<h3><a id="user-content-setter-injection---injecting-literal-values-from-a-properties-file" class="anchor" aria-hidden="true" href="#setter-injection---injecting-literal-values-from-a-properties-file"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Setter Injection - Injecting literal values from a Properties File</h3>
<p>We can also import literal values from another file so we don't have to hard code them inside the XML applicationContext</p>
<p>Steps:</p>
<ol>
<li>Create a Properties file</li>
<li>Load Properties file in Spring config file</li>
<li>Reference values from the Properties file</li>
</ol>
<p>We create a plain text file: myfile.properties<br>
and we type like in bash:
foo.email=<a href="mailto:myemail@mail.com">myemail@mail.com</a>
foo.team=My Sports Team</p>
<p>Then in the applicationContext file:</p>
<div class="highlight highlight-text-xml"><pre>&lt;<span class="pl-ent">context</span><span class="pl-ent">:</span><span class="pl-ent">property-placeholder</span> <span class="pl-e">location</span>=<span class="pl-s"><span class="pl-pds">"</span>classpath:myfile.properties<span class="pl-pds">"</span></span>&gt;
&lt;<span class="pl-ent">property</span> <span class="pl-e">name</span>=<span class="pl-s"><span class="pl-pds">"</span>emailAddress<span class="pl-pds">"</span></span> <span class="pl-e">value</span>=<span class="pl-s"><span class="pl-pds">"</span>${foo.email}<span class="pl-pds">"</span></span>&gt;</pre></div>
<p>Funny enough, it's like having a config file for the config file</p>
<hr>
<h2><a id="user-content-6---spring-bean-scopes-and-lifecycle" class="anchor" aria-hidden="true" href="#6---spring-bean-scopes-and-lifecycle"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>6 - SPRING BEAN SCOPES AND LIFECYCLE</h2>
<h3><a id="user-content-bean-scopes---overview" class="anchor" aria-hidden="true" href="#bean-scopes---overview"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Bean Scopes - Overview</h3>
<p>Scope refers to the lifecycle of the bean</p>
<ul>
<li>how long does the bean live?</li>
<li>how many instances are created?</li>
<li>how is the bean shared?</li>
</ul>
<p>The default scope is singleton</p>
<ul>
<li>The Spring Container creates only one instance of the bean</li>
<li>It is cached in memory</li>
<li>All requests for the bean will reference a same shared bean</li>
</ul>
<p>Example:</p>
<div class="highlight highlight-source-java"><pre><span class="pl-smi">Coach</span> alphaCoach <span class="pl-k">=</span> context<span class="pl-k">.</span>getBean(<span class="pl-s"><span class="pl-pds">"</span>myCoach<span class="pl-pds">"</span></span>, <span class="pl-smi">Coach</span><span class="pl-k">.</span>class);
<span class="pl-smi">Coach</span> betaCoach <span class="pl-k">=</span> context<span class="pl-k">.</span>getBean(<span class="pl-s"><span class="pl-pds">"</span>myCoach<span class="pl-pds">"</span></span>, <span class="pl-smi">Coach</span><span class="pl-k">.</span>class);</pre></div>
<p>These 2 refer to the same instance<br>
-&gt; static instances</p>
<p>We can use the "scope" attribute to explicitly specify the scope:</p>
<ul>
<li>singleton - single shared instance</li>
<li>propotype - new instance for each container request</li>
<li>request - scoped to an http web request</li>
<li>session - scoped to an http web session</li>
<li>global-session - scoped to a global http web session</li>
</ul>
<h3><a id="user-content-bean-scopes---write-some-code" class="anchor" aria-hidden="true" href="#bean-scopes---write-some-code"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Bean Scopes - Write some code</h3>
<p>Singleton - same instance, same location in memory
Prototype - different instances and locations in memory</p>
<h3><a id="user-content-bean-lifecycle---overview" class="anchor" aria-hidden="true" href="#bean-lifecycle---overview"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Bean Lifecycle - Overview</h3>
<p>This is the overall Spring process:</p>
<ol>
<li>container starts</li>
<li>beans are instantiated</li>
<li>dependencies are injected</li>
<li>internal spring processing</li>
<li>Custom Init method</li>
<li>Application runtime until shutdown</li>
<li>Application is shutdown</li>
<li>Custom Destroy Method</li>
<li>Stop</li>
</ol>
<p>In steps 5 and 8 we can define custom methods, typically we can use them to:</p>
<ul>
<li>call some custom business logic methods</li>
<li>set up / clean up custom handles to resources (db, sockets, files, etc.)</li>
</ul>
<p>We call them with attributes in the <code>&lt;bean&gt;</code> tag:</p>
<ul>
<li>init-method="myInitMethod"</li>
<li>destroy-method="myDestroyMethod"</li>
</ul>
<p>Steps:</p>
<ol>
<li>Define methods for init and destroy</li>
<li>Configure the method names in Spring config file</li>
</ol>
<p>Notes regarding init and destroy methods when using XML configuration:</p>
<ul>
<li>methods can have any access modifier (public, private, protected)</li>
<li>methods can have any return type. However, we cannot capture any return value, so typically use "void" anyway</li>
<li>methods cannot accept any arguments</li>
<li>for prototype beans, the destroy method does not work (Spring does not manage the complete lifecycle of a prototype bean)</li>
</ul>
<hr>
<h2><a id="user-content-7---spring-configuration-with-java-annotations---ioc" class="anchor" aria-hidden="true" href="#7---spring-configuration-with-java-annotations---ioc"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>7 - SPRING CONFIGURATION WITH JAVA ANNOTATIONS - IoC</h2>
<h3><a id="user-content-annotations-overview---component-scanning" class="anchor" aria-hidden="true" href="#annotations-overview---component-scanning"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Annotations Overview - Component Scanning</h3>
<p>What are Java annotations?</p>
<ul>
<li>special markers added to Java classes</li>
<li>provide meta data about the class</li>
<li>processed at compile time or runtime</li>
</ul>
<p>Why?</p>
<ul>
<li>XML can be very verbose (ie: when 30+ beans)</li>
<li>Annotations minimize XML configuration</li>
</ul>
<div class="highlight highlight-source-java"><pre><span class="pl-k">@Component</span>(<span class="pl-s"><span class="pl-pds">"</span>myId<span class="pl-pds">"</span></span>)</pre></div>
<p>Spring is going to scan our classes looking for annotations and when it find one, it register the beans from it with id "myId"</p>
<p>Development steps:</p>
<ol>
<li>enable component scanning in Spring config file</li>
<li>add @Component to our classes</li>
<li>retrieve bean from Spring container</li>
</ol>
<h3><a id="user-content-write-some-code" class="anchor" aria-hidden="true" href="#write-some-code"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Write some code</h3>
<ol>
<li>enable component scanning in Spring config file</li>
</ol>
<p>add this tag:</p>
<div class="highlight highlight-text-xml"><pre>&lt;<span class="pl-ent">context</span><span class="pl-ent">:</span><span class="pl-ent">component-scan</span> <span class="pl-e">base-package</span>=<span class="pl-s"><span class="pl-pds">"</span>com.motlaweb.springdemo<span class="pl-pds">"</span></span> /&gt;</pre></div>
<ol start="2">
<li>Annotate the class</li>
</ol>
<div class="highlight highlight-source-java"><pre><span class="pl-k">@Component</span>(<span class="pl-s"><span class="pl-pds">"</span>theIdOfTheClass<span class="pl-pds">"</span></span>)
<span class="pl-k">public</span> <span class="pl-k">class</span> <span class="pl-en">MyClassName</span> {}</pre></div>
<ol start="3">
<li>retrieve the bean</li>
</ol>
<div class="highlight highlight-source-java"><pre><span class="pl-smi">Coach</span> theCoach <span class="pl-k">=</span> context<span class="pl-k">.</span>getBean(<span class="pl-s"><span class="pl-pds">"</span>theIdOfTheClass<span class="pl-pds">"</span></span>, <span class="pl-smi">Coach</span><span class="pl-k">.</span>class);</pre></div>
<p>Overall, the Main class is the same, only difference is in the annotations in the classes, and no <code>&lt;bean&gt;</code> in the XML</p>
<h3><a id="user-content-default-bean-id" class="anchor" aria-hidden="true" href="#default-bean-id"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Default bean id</h3>
<p>If we don't specify an id in the annotation, the default Id will be the name of the class with lower first letter:</p>
<div class="highlight highlight-source-java"><pre><span class="pl-k">@Component</span>
<span class="pl-k">public</span> <span class="pl-k">class</span> <span class="pl-en">MyClassName</span> {}</pre></div>
<p>Here the id will be "myClassName"</p>
<p>EXCEPTION: when the className starts with 2+ capital letters. Exemple: RESTService
In this case, the default bean name remains the same (RESTService)</p>
<hr>
<h2><a id="user-content-8---spring-configuration-with-java-annotations---di" class="anchor" aria-hidden="true" href="#8---spring-configuration-with-java-annotations---di"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>8 - SPRING CONFIGURATION WITH JAVA ANNOTATIONS - DI</h2>
<p>For DI with annotations, Spring uses Auto-wiring:</p>
<ul>
<li>it looks for a class/interface that matches the property</li>
<li>by scanning classes with @Component</li>
<li>anyone implements the dependency interface?</li>
<li>if so, it injects it automatically</li>
</ul>
<p>With auto-wiring, there are 3 types of injections</p>
<ul>
<li>constructor</li>
<li>setter</li>
<li>field</li>
</ul>
<h3><a id="user-content-constructor-injection" class="anchor" aria-hidden="true" href="#constructor-injection"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Constructor injection</h3>
<p>Process</p>
<ol>
<li>define the dependency interface and class</li>
<li>create a constructor in the class for injections</li>
<li>configure the dependency injection with @Autowired annotation in the constructor</li>
</ol>
<h3><a id="user-content-setter-injection" class="anchor" aria-hidden="true" href="#setter-injection"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Setter injection</h3>
<p>Inject dependencies by calling setter methods on the class</p>
<p>Process</p>
<ol>
<li>define the dependency interface and class</li>
<li>create a setter method in the class for injections</li>
<li>configure the dependency injection with @Autowired annotation in the setter method</li>
</ol>
<blockquote>
<p>NOTE: Actually we can use ANY METHOD with @Autowired, not necessarily a setter method</p>
</blockquote>
<h3><a id="user-content-field-injection" class="anchor" aria-hidden="true" href="#field-injection"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Field injection</h3>
<p>Inject dependencies by setting field values on your class directly (even private fields).<br>
This is accomplished using a technique named Java Reflection</p>
<p>Process</p>
<ol>
<li>define the dependency interface and class</li>
<li>configure the dependency injection with Autowired applied directly to the field (no need for a setter method)</li>
</ol>
<p>Spring autowires the field by instantiating afortuneService automatically</p>
<h3><a id="user-content-which-injection-type-should-we-use" class="anchor" aria-hidden="true" href="#which-injection-type-should-we-use"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Which Injection Type should we use?</h3>
<p>Best advice is to choose a style and stay consistent throughout the project<br>
All 3 types provide same functionality</p>
<h3><a id="user-content-qualifiers-for-dependency-injection" class="anchor" aria-hidden="true" href="#qualifiers-for-dependency-injection"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Qualifiers for Dependency Injection</h3>
<p>With @Autowiring, Spring automatically injects the bean. But what if there are multiple implementations of the same Dependency?</p>
<p>For example: HappyFortuneService, RandomFortuneService, BadFortuneService, LuckyFortuneService, etc. all with @Component</p>
<p>In such cases, we need to tell Spring which one to use. We do so with the @Qualifier annotation with its default bean Id (class name with small initial cap)</p>
<p>This @Qualifier annotation can be applied to all cases</p>
<ul>
<li>constructor injection</li>
<li>setter injection</li>
<li>field injection</li>
</ul>
<div class="highlight highlight-source-java"><pre><span class="pl-k">@Autowired</span>
<span class="pl-k">@Qualifier</span>(<span class="pl-s"><span class="pl-pds">"</span>randomService<span class="pl-pds">"</span></span>)
<span class="pl-k">private</span> <span class="pl-smi">Fortune</span> fortuneService;</pre></div>
<blockquote>
<p>NOTE: for constructor method, the @Qualifier goes inside the argument:</p>
</blockquote>
<div class="highlight highlight-source-java"><pre><span class="pl-k">@Autowired</span>
    <span class="pl-k">public</span> TennisCoach(<span class="pl-k">@Qualifier</span>(<span class="pl-s"><span class="pl-pds">"</span>randomFortuneService<span class="pl-pds">"</span></span>) <span class="pl-smi">FortuneService</span> theFortuneService) {
        <span class="pl-smi">System</span><span class="pl-k">.</span>out<span class="pl-k">.</span>println(<span class="pl-s"><span class="pl-pds">"</span>&gt;&gt; TennisCoach: inside constructor using @autowired and @qualifier<span class="pl-pds">"</span></span>);
        fortuneService <span class="pl-k">=</span> theFortuneService;
    }</pre></div>
<h3><a id="user-content-setter-injection-with-annotations---injecting-literal-values-from-a-properties-file" class="anchor" aria-hidden="true" href="#setter-injection-with-annotations---injecting-literal-values-from-a-properties-file"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Setter Injection with Annotations - Injecting literal values from a Properties File</h3>
<p>We can also import literal values from the Properties file using Annotations</p>
<p>Steps</p>
<ol>
<li>Create a Properties file</li>
<li>Load Properties file in Spring config file</li>
</ol>
<div class="highlight highlight-text-xml"><pre>&lt;<span class="pl-ent">context</span><span class="pl-ent">:</span><span class="pl-ent">property-placeholder</span> <span class="pl-e">location</span>=<span class="pl-s"><span class="pl-pds">"</span>classpath:sport.properties<span class="pl-pds">"</span></span>/&gt;</pre></div>
<ol start="3">
<li>Reference values from the Properties file</li>
</ol>
<div class="highlight highlight-source-java"><pre>    <span class="pl-k">@Value</span>(<span class="pl-s"><span class="pl-pds">"</span>${foo.email}<span class="pl-pds">"</span></span>)
    <span class="pl-k">private</span> <span class="pl-smi">String</span> email;
        
    <span class="pl-k">@Value</span>(<span class="pl-s"><span class="pl-pds">"</span>${foo.team}<span class="pl-pds">"</span></span>)
    <span class="pl-k">private</span> <span class="pl-smi">String</span> team;</pre></div>
<p>We create a plain text file: myfile.properties
and we type like in bash:
<em>foo.email=<a href="mailto:myemail@mail.com">myemail@mail.com</a></em>
<em>foo.team=My Sports Team</em></p>
<hr>
<h2><a id="user-content-9---spring-configuration-with-java-annotations---bean-scopes-and-lifecycle-methods" class="anchor" aria-hidden="true" href="#9---spring-configuration-with-java-annotations---bean-scopes-and-lifecycle-methods"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>9 - SPRING CONFIGURATION WITH JAVA ANNOTATIONS - BEAN SCOPES AND LIFECYCLE METHODS</h2>
<h3><a id="user-content-scope-annotation---overview" class="anchor" aria-hidden="true" href="#scope-annotation---overview"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>@Scope Annotation - Overview</h3>
<p>Same as for XML configuration, default scope is Singleton</p>
<p>We can specify a different scope with the @Scope annotation (for the bean)</p>
<div class="highlight highlight-source-java"><pre><span class="pl-k">@Component</span>
<span class="pl-k">@Scope</span>(<span class="pl-s"><span class="pl-pds">"</span>prototype<span class="pl-pds">"</span></span>)
<span class="pl-k">public</span> <span class="pl-k">class</span> <span class="pl-en">TennisCoach</span> <span class="pl-k">implements</span> <span class="pl-e">Coach</span> {
    <span class="pl-c1">...</span>
}</pre></div>
<h3><a id="user-content-bean-lifecycle-with-annotations---overview" class="anchor" aria-hidden="true" href="#bean-lifecycle-with-annotations---overview"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Bean Lifecycle with Annotations - Overview</h3>
<p>We can add some custom code during bean intitliazation
For that we use annotations @PostConstruct and @PreDestroy</p>
<p>Process</p>
<ol>
<li>define methods for init and destroy</li>
<li>add annotations @PostConstruct and @PreDestroy to the methods</li>
</ol>
<p>Same remarks as for XML configuration:</p>
<ul>
<li>methods can have any access modifier (public, private, protected)</li>
<li>methods can have any return type. However, we cannot capture any return value, so typically use "void" anyway</li>
<li>methods cannot accept any arguments</li>
<li>for prototype beans, the destroy method does not work (Spring does not manage the complete lifecycle of a prototype bean)</li>
</ul>
<hr>
<h2><a id="user-content-10---spring-configuration-with-java-code" class="anchor" aria-hidden="true" href="#10---spring-configuration-with-java-code"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>10 - SPRING CONFIGURATION WITH JAVA CODE</h2>
<h3><a id="user-content-spring-configuration-with-java-code---overview" class="anchor" aria-hidden="true" href="#spring-configuration-with-java-code---overview"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Spring Configuration with Java code - Overview</h3>
<p>In this case we don't need an XML at all</p>
<p>Reminder 3 ways of configuring the Spring container:</p>
<ol>
<li>Full XML config</li>
<li>Annotations (XML component-scan)</li>
<li>Java source code</li>
</ol>
<p>Process</p>
<ol>
<li>create a Java class and annotate it as @Configuration</li>
<li>add component scanning support for a package with @ComponentScan (optional)</li>
<li>read Spring Java configuration class (AnnotationConfigApplicationContext)</li>
<li>retrieve bean from Spring container (getBean())</li>
</ol>
<p>There are 2 ways to create beans:</p>
<ol>
<li>with @ComponentScan</li>
<li>with manual bean creation @Bean (see next paragraph)</li>
</ol>
<h3><a id="user-content-defining-spring-beans-with-java-code---overview" class="anchor" aria-hidden="true" href="#defining-spring-beans-with-java-code---overview"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Defining Spring beans with Java code - Overview</h3>
<p>Process</p>
<ol>
<li>define method to expose the bean (the name of the method will be the bean Id) in the Config class</li>
<li>inject bean dependencies (other @Bean's)</li>
<li>read Spring Java configuration class</li>
<li>retrieve bean from Spring container</li>
</ol>
<h3><a id="user-content-injecting-values-from-a-properties-file---overview" class="anchor" aria-hidden="true" href="#injecting-values-from-a-properties-file---overview"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Injecting values from a Properties file - Overview</h3>
<p>Process</p>
<ol>
<li>create Properties file</li>
<li>load Properties file in Spring config with @PropertySource("classpath:filename")</li>
<li>reference values from Properties file with @Value("${varName}")</li>
</ol>
<hr>
<h2><a id="user-content-11---spring-mvc---building-spring-web-apps" class="anchor" aria-hidden="true" href="#11---spring-mvc---building-spring-web-apps"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>11 - SPRING MVC - BUILDING SPRING WEB APPS</h2>
<p><a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/web.html" rel="nofollow">https://docs.spring.io/spring/docs/current/spring-framework-reference/web.html</a></p>
<h3><a id="user-content-spring-mvc-overview" class="anchor" aria-hidden="true" href="#spring-mvc-overview"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Spring MVC Overview</h3>
<p>Framework for building web applications in Java, based on the MVC design pattern<br>
It leverages features of the Spring Framework Core (IoC)</p>
<p>Benefits:</p>
<ul>
<li>Spring way of building web apps UI</li>
<li>leverage a set of reusable UI components</li>
<li>help manage application state for web requests (sessions, etc.)</li>
<li>process form data (validation, conversion, etc.)</li>
<li>flexible configuration for the view layer</li>
</ul>
<h3><a id="user-content-spring-mvc---behind-the-scenes" class="anchor" aria-hidden="true" href="#spring-mvc---behind-the-scenes"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Spring MVC - Behind the Scenes</h3>
<p>When we receive an incoming request from the browser, it encounters the Spring MVC Front Controller (DispatcherServlet).<br>
This FC transfers the request to the Controller programmed by us, which contains our business logic.</p>
<p>The Controller manipulates the data through Models and sends it back to the FC, which will turn it into the View template (HTML, JSP...).</p>
<p>Components of a Spring MVC app:</p>
<ul>
<li>A set of webpages to layout UI components</li>
<li>A collection of Spring beans (controllers, services...)</li>
<li>Spring Configuration (XML files, Annotations or Java)</li>
</ul>
<p>Interaction with the client's browser is done through the DispatcherServlet, which is provided by Spring. What we have to develop is the MVC:</p>
<ul>
<li>Model objects
<ul>
<li>contains the data</li>
<li>mapping towards a backend system (database, web service, etc.)</li>
<li>can be an object, bean, collection...</li>
</ul>
</li>
<li>View templates
<ul>
<li>displays UI layout in the browser (typically html, jsp, jstl)</li>
<li>may include data passed from the model</li>
<li>very flexible: can be of many types, use templating systems (velocity, thymeleaf, etc.)</li>
</ul>
</li>
<li>Controller classes
<ul>
<li>contain the business logic</li>
<li>handles requests</li>
<li>manages the data from/to the model</li>
<li>sends to appropiate view template</li>
</ul>
</li>
</ul>
<h3><a id="user-content-spring-mvc-configuration" class="anchor" aria-hidden="true" href="#spring-mvc-configuration"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Spring MVC Configuration</h3>
<ol>
<li>Create a new Web Project (Java EE)
<ol>
<li>add Spring jars</li>
</ol>
</li>
<li>Add configurations to file WEB-INF/web.xml
<ol>
<li>configure Spring MVC Dispatcher Servlet</li>
<li>set up URL mappings to Spring MVC Dispatcher Servlet</li>
</ol>
</li>
<li>Add configurations to file WEB-INF/spring-mvc-demo-servlet.xml
<ol>
<li>add support for Spring component scanning</li>
<li>add support for conversion, formatting and validation</li>
<li>configure Spring MVC view resolver</li>
</ol>
</li>
</ol>
<p>in <code>web.xml</code>:</p>
<div class="highlight highlight-text-xml"><pre><span class="pl-c"><span class="pl-c">&lt;!--</span> Spring MVC Configs <span class="pl-c">--&gt;</span></span>

<span class="pl-c"><span class="pl-c">&lt;!--</span> Step 1: Configure Spring MVC Dispatcher Servlet <span class="pl-c">--&gt;</span></span>
&lt;<span class="pl-ent">servlet</span>&gt;
&lt;<span class="pl-ent">servlet-name</span>&gt;dispatcher&lt;/<span class="pl-ent">servlet-name</span>&gt;
&lt;<span class="pl-ent">servlet-class</span>&gt;org.springframework.web.servlet.DispatcherServlet&lt;/<span class="pl-ent">servlet-class</span>&gt;
&lt;<span class="pl-ent">init-param</span>&gt;
<span class="pl-c"><span class="pl-c">&lt;!--</span> application context configuration file <span class="pl-c">--&gt;</span></span>
&lt;<span class="pl-ent">param-name</span>&gt;contextConfigLocation&lt;/<span class="pl-ent">param-name</span>&gt;
&lt;<span class="pl-ent">param-value</span>&gt;/WEB-INF/spring-mvc-demo-servlet.xml&lt;/<span class="pl-ent">param-value</span>&gt;
&lt;/<span class="pl-ent">init-param</span>&gt;
&lt;<span class="pl-ent">load-on-startup</span>&gt;1&lt;/<span class="pl-ent">load-on-startup</span>&gt;
&lt;/<span class="pl-ent">servlet</span>&gt;

<span class="pl-c"><span class="pl-c">&lt;!--</span> Step 2: Set up URL mapping for Spring MVC Dispatcher Servlet <span class="pl-c">--&gt;</span></span>
&lt;<span class="pl-ent">servlet-mapping</span>&gt;
&lt;<span class="pl-ent">servlet-name</span>&gt;dispatcher&lt;/<span class="pl-ent">servlet-name</span>&gt;
&lt;<span class="pl-ent">url-pattern</span>&gt;/&lt;/<span class="pl-ent">url-pattern</span>&gt;
&lt;/<span class="pl-ent">servlet-mapping</span>&gt;</pre></div>
<p>in <code>spring-mvc-demo-servlet.xml</code>:</p>
<div class="highlight highlight-text-xml"><pre><span class="pl-c"><span class="pl-c">&lt;!--</span> Step 3: Add support for component scanning <span class="pl-c">--&gt;</span></span>
&lt;<span class="pl-ent">context</span><span class="pl-ent">:</span><span class="pl-ent">component-scan</span> <span class="pl-e">base-package</span>=<span class="pl-s"><span class="pl-pds">"</span>com.luv2code.springdemo<span class="pl-pds">"</span></span> /&gt;

<span class="pl-c"><span class="pl-c">&lt;!--</span> Step 4: Add support for conversion, formatting and validation support <span class="pl-c">--&gt;</span></span>
&lt;<span class="pl-ent">mvc</span><span class="pl-ent">:</span><span class="pl-ent">annotation-driven</span>/&gt;

<span class="pl-c"><span class="pl-c">&lt;!--</span> Step 5: Define Spring MVC view resolver. This tells Spring where to look for the template files, and how they are named <span class="pl-c">--&gt;</span></span>
&lt;<span class="pl-ent">bean</span>
class=<span class="pl-s"><span class="pl-pds">"</span>org.springframework.web.servlet.view.InternalResourceViewResolver<span class="pl-pds">"</span></span>&gt;
&lt;<span class="pl-ent">property</span> <span class="pl-e">name</span>=<span class="pl-s"><span class="pl-pds">"</span>prefix<span class="pl-pds">"</span></span> <span class="pl-e">value</span>=<span class="pl-s"><span class="pl-pds">"</span>/WEB-INF/view/<span class="pl-pds">"</span></span> /&gt;
&lt;<span class="pl-ent">property</span> <span class="pl-e">name</span>=<span class="pl-s"><span class="pl-pds">"</span>suffix<span class="pl-pds">"</span></span> <span class="pl-e">value</span>=<span class="pl-s"><span class="pl-pds">"</span>.jsp<span class="pl-pds">"</span></span> /&gt;
&lt;/<span class="pl-ent">bean</span>&gt;</pre></div>
<p>Plus:</p>
<ol>
<li>Add necessary JAR files
<ol>
<li>javax.servlet.jsp.jstl-1.2.1.jar</li>
<li>javax.servlet.jsp.jstl-api-1.2.1.jar</li>
</ol>
</li>
<li>Create folder WEB-INF/view/</li>
</ol>
<hr>
<h2><a id="user-content-12---spring-mvc---creating-controllers-and-views" class="anchor" aria-hidden="true" href="#12---spring-mvc---creating-controllers-and-views"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>12 - SPRING MVC - CREATING CONTROLLERS AND VIEWS</h2>
<h3><a id="user-content-creating-a-spring-home-controller-and-view---overview" class="anchor" aria-hidden="true" href="#creating-a-spring-home-controller-and-view---overview"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Creating a Spring Home Controller and View - Overview</h3>
<p>First example: homepage</p>
<p>Development process:</p>
<ol>
<li>create controller class</li>
<li>define controller method (the name can be anything we want, it's not used, only the @RequestMapping is used)</li>
<li>add request mapping to controller method</li>
<li>return view name</li>
<li>develop view page</li>
</ol>
<h3><a id="user-content-write-some-code-1" class="anchor" aria-hidden="true" href="#write-some-code-1"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Write some code</h3>
<ol>
<li>create a new package</li>
</ol>
<h3><a id="user-content-reading-html-form-data" class="anchor" aria-hidden="true" href="#reading-html-form-data"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Reading HTML Form Data</h3>
<p>Process</p>
<ol>
<li>Create controller class</li>
<li>Show HTML form
<ol>
<li>create controller method to show the HTML form
<ol>
<li>add RequestMapping</li>
<li>return view name</li>
</ol>
</li>
<li>create view page for HTML form</li>
</ol>
</li>
<li>Process HTML form</li>
<li>create controller method to process the HTML form
<ol>
<li>add RequestMapping</li>
<li>return view name</li>
</ol>
</li>
<li>create view page for Form confirmation</li>
</ol>
<h3><a id="user-content-adding-data-to-the-spring-model" class="anchor" aria-hidden="true" href="#adding-data-to-the-spring-model"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Adding Data to the Spring Model</h3>
<ul>
<li>The Model is a container for our application data</li>
<li>In the Controller we can put anything in the model: Strings, Objects, database info, etc.</li>
<li>Our View pages (JSP) can access data from the model</li>
</ul>
<div class="highlight highlight-source-java"><pre><span class="pl-c"><span class="pl-c">//</span> new controller method to read form data and add data to the model</span>
    
    <span class="pl-k">@RequestMapping</span>(<span class="pl-s"><span class="pl-pds">"</span>/processFormVersionTwo<span class="pl-pds">"</span></span>)
    <span class="pl-k">public</span> <span class="pl-smi">String</span> letsShoutDude(<span class="pl-smi">HttpServletRequest</span> request, <span class="pl-smi">Model</span> model) {
        
        <span class="pl-c"><span class="pl-c">//</span> read the request parameter from the HTML form</span>
        <span class="pl-smi">String</span> theName <span class="pl-k">=</span> request<span class="pl-k">.</span>getParameter(<span class="pl-s"><span class="pl-pds">"</span>studentName<span class="pl-pds">"</span></span>);
        
        <span class="pl-c"><span class="pl-c">//</span> convert the data to all caps</span>
        theName <span class="pl-k">=</span> theName<span class="pl-k">.</span>toUpperCase();
        
        <span class="pl-c"><span class="pl-c">//</span> create the message</span>
        <span class="pl-smi">String</span> result <span class="pl-k">=</span> <span class="pl-s"><span class="pl-pds">"</span>Yo! <span class="pl-pds">"</span></span> <span class="pl-k">+</span> theName;
        
        <span class="pl-c"><span class="pl-c">//</span> add message to the model. "message" is the identifier used in the Jsp view through ${message}</span>
        model<span class="pl-k">.</span>addAttribute(<span class="pl-s"><span class="pl-pds">"</span>message<span class="pl-pds">"</span></span>, result);
        
        <span class="pl-k">return</span> <span class="pl-s"><span class="pl-pds">"</span>helloworld<span class="pl-pds">"</span></span>;
    }</pre></div>
<p><em>HttpServletRequest</em> is used to read form data
Model is just a container for our data, it comes empty and then we can data to it. Data can be in any form: a string, but also any other Object, List, etc.</p>
<h3><a id="user-content-how-to-use-css-javascript-and-images-in-a-spring-mvc-web-app---review" class="anchor" aria-hidden="true" href="#how-to-use-css-javascript-and-images-in-a-spring-mvc-web-app---review"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>How to use CSS, JavaScript and Images in a Spring MVC Web App - <strong>review</strong></h3>
<p>Any static resource is processed as a URL Mapping in Spring MVC. You can configure references to static resources in the spring-mvc-demo-servlet.xml.</p>
<p>In my example, I'm going to have the following directory structure:</p>
<p><a target="_blank" rel="noopener noreferrer" href="/moltaweb/cursos/blob/master/images/spring_folder.png"><img src="/moltaweb/cursos/raw/master/images/spring_folder.png" alt="Spring Folder" style="max-width:100%;"></a></p>
<p>I chose to put everything in the "resources" directory. But you can use any name for "resources", such as "assets", "foobar" etc. Also, you can give any name that you want for the subdirectories under "resources".</p>
<hr>
<p>Step 1: Add the following entry to your Spring MVC configuration file <code>spring-mvc-demo-servlet.xml</code></p>
<p>You can place this entry anywhere in your Spring MVC config file.</p>
<div class="highlight highlight-text-xml"><pre>&lt;<span class="pl-ent">mvc</span><span class="pl-ent">:</span><span class="pl-ent">resources</span> <span class="pl-e">mapping</span>=<span class="pl-s"><span class="pl-pds">"</span>/resources/**<span class="pl-pds">"</span></span> <span class="pl-e">location</span>=<span class="pl-s"><span class="pl-pds">"</span>/resources/<span class="pl-pds">"</span></span>&gt;&lt;/<span class="pl-ent">mvc</span><span class="pl-ent">:</span><span class="pl-ent">resources</span>&gt;</pre></div>
<p>Step 2: Now in your view pages, you can access the static files using this syntax:</p>
<div class="highlight highlight-text-xml"><pre>&lt;<span class="pl-ent">img</span> <span class="pl-e">src</span>=<span class="pl-s"><span class="pl-pds">"</span>${pageContext.request.contextPath}/resources/images/spring-logo.png<span class="pl-pds">"</span></span>&gt;</pre></div>
<p>You need to use the JSP expression <code>${pageContext.request.contextPath}</code> to access the correct root directory for your web application.</p>
<p>Apply the same technique for reading CSS and JavaScript.</p>
<hr>
<p>Here's a full example that reads CSS, JavaScript and images.</p>
<div class="highlight highlight-text-html-basic"><pre>&lt;!DOCTYPE html&gt; 
&lt;<span class="pl-ent">html</span>&gt;

&lt;<span class="pl-ent">head</span>&gt;
    &lt;<span class="pl-ent">link</span> <span class="pl-e">rel</span>=<span class="pl-s"><span class="pl-pds">"</span>stylesheet<span class="pl-pds">"</span></span> <span class="pl-e">type</span>=<span class="pl-s"><span class="pl-pds">"</span>text/css<span class="pl-pds">"</span></span>          
           <span class="pl-e">href</span>=<span class="pl-s"><span class="pl-pds">"</span>${pageContext.request.contextPath}/resources/css/my-test.css<span class="pl-pds">"</span></span>&gt;
    &lt;<span class="pl-ent">script</span> <span class="pl-e">src</span>=<span class="pl-s"><span class="pl-pds">"</span>${pageContext.request.contextPath}/resources/js/simple-test.js<span class="pl-pds">"</span></span>&gt;&lt;/<span class="pl-ent">script</span>&gt;
&lt;/<span class="pl-ent">head</span>&gt;

&lt;<span class="pl-ent">body</span>&gt;
    &lt;<span class="pl-ent">h2</span>&gt;Spring MVC Demo - Home Page&lt;/<span class="pl-ent">h2</span>&gt;
    &lt;<span class="pl-ent">a</span> <span class="pl-e">href</span>=<span class="pl-s"><span class="pl-pds">"</span>hello<span class="pl-pds">"</span></span>&gt;Plain Hello World&lt;/<span class="pl-ent">a</span>&gt;
    &lt;<span class="pl-ent">br</span>&gt;&lt;<span class="pl-ent">br</span>&gt;
    &lt;<span class="pl-ent">img</span> <span class="pl-e">src</span>=<span class="pl-s"><span class="pl-pds">"</span>${pageContext.request.contextPath}/resources/images/spring-logo.png<span class="pl-pds">"</span></span> /&gt;
    &lt;<span class="pl-ent">br</span>&gt;&lt;<span class="pl-ent">br</span>&gt;
    &lt;<span class="pl-ent">input</span> <span class="pl-e">type</span>=<span class="pl-s"><span class="pl-pds">"</span>button<span class="pl-pds">"</span></span> <span class="pl-e">onclick</span>=<span class="pl-s"><span class="pl-pds">"</span>doSomeWork()<span class="pl-pds">"</span></span> <span class="pl-e">value</span>=<span class="pl-s"><span class="pl-pds">"</span>Click Me<span class="pl-pds">"</span></span>/&gt;
&lt;/<span class="pl-ent">body</span>&gt;

&lt;/<span class="pl-ent">html</span>&gt;</pre></div>
<h3><a id="user-content-deploying-your-app-to-tomcat-as-a-web-application-archive-war-file" class="anchor" aria-hidden="true" href="#deploying-your-app-to-tomcat-as-a-web-application-archive-war-file"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Deploying your App to Tomcat as a Web Application Archive (WAR) file</h3>
<p>When you deploy your Java web apps, you can make use of a Web Application Archive (WAR) file.</p>
<p>The Web Application Archive (WAR) file is a compressed version of your web application. It uses the zip file format but the file has the .war extension.</p>
<p>If you are using Eclipse, then the best way to visualize it is think of your "WebContent" directory being compressed as a zip file with the .war extension.</p>
<p>This includes all of your web pages, images, css etc. It also includes the WEB-INF directory which includes your classes in WEB-INF/classes and supporting JAR files in WEB-INF/lib.</p>
<p>The WAR file format is part of the Java EE / Servlet specification. As a result, all Java EE servers support this format (ie jboss, weblogic, websphere, glassfish and tomcat).</p>
<p>Below, I provide steps on how to create a WAR file in Eclipse. I also show how to deploy the WAR file on Tomcat.</p>
<hr>
<ol>
<li>In Eclipse, stop Tomcat</li>
<li>Right-click your project and select Export &gt; WAR File</li>
<li>In the Destination field, enter: /mycoolapp.war</li>
<li>Outside of Eclipse, start Tomcat</li>
</ol>
<ul>
<li>If you are using MS Windows, then you should find it on the Start menu</li>
</ul>
<ol start="5">
<li>Make sure Tomcat is up and running by visiting: <a href="http://localhost:8080" rel="nofollow">http://localhost:8080</a></li>
<li>Deploy your new WAR file by copying it to \webapps
Give it about 10-15 seconds to make the deployment. You'll know the deployment is over because you'll see a new folder created in webapps ... with your WAR file name.</li>
<li>Visit your new app. If your war file was: mycoolapp.war then you can access it with:  <a href="http://localhost:8080/mycoolapp/" rel="nofollow">http://localhost:8080/mycoolapp/</a></li>
</ol>
<hr>
<h2><a id="user-content-13---spring-mvc---request-params-and-request-mappings" class="anchor" aria-hidden="true" href="#13---spring-mvc---request-params-and-request-mappings"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>13 - SPRING MVC - REQUEST PARAMS AND REQUEST MAPPINGS</h2>
<h3><a id="user-content-binding-request-params" class="anchor" aria-hidden="true" href="#binding-request-params"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Binding Request Params</h3>
<p>Another way to read form data is by using the annotation @RequestParam</p>
<p>The idea is to automatically get the parameter and bind it to the variable. It's a shortcut for:</p>
<div class="highlight highlight-source-java"><pre><span class="pl-k">@RequestMapping</span>(<span class="pl-s"><span class="pl-pds">"</span>/processFormVersionTwo<span class="pl-pds">"</span></span>)
<span class="pl-k">public</span> <span class="pl-smi">String</span> letsShoutDude(<span class="pl-smi">HttpServletRequest</span> request, <span class="pl-smi">Model</span> model) {
        
    <span class="pl-c"><span class="pl-c">//</span> read the request parameter from the HTML form</span>
    <span class="pl-smi">String</span> theName <span class="pl-k">=</span> request<span class="pl-k">.</span>getParameter(<span class="pl-s"><span class="pl-pds">"</span>studentName<span class="pl-pds">"</span></span>);</pre></div>
<p>By doing directly:</p>
<div class="highlight highlight-source-java"><pre><span class="pl-k">@RequestMapping</span>(<span class="pl-s"><span class="pl-pds">"</span>/processFormVersionThree<span class="pl-pds">"</span></span>)
<span class="pl-k">public</span> <span class="pl-smi">String</span> letsShoutDude(<span class="pl-k">@RequestPAram</span>(<span class="pl-s"><span class="pl-pds">"</span>studentName<span class="pl-pds">"</span></span>) <span class="pl-smi">String</span> theName, <span class="pl-smi">Model</span> model) {

<span class="pl-c"><span class="pl-c">/*</span> NOT NECESSARY ANYMORE      </span>
<span class="pl-c">    // read the request parameter from the HTML form</span>
<span class="pl-c">    String theName = request.getParameter("studentName");</span>
<span class="pl-c"><span class="pl-c">*/</span></span>      </pre></div>
<h3><a id="user-content-controller-level-request-mapping" class="anchor" aria-hidden="true" href="#controller-level-request-mapping"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Controller Level Request Mapping</h3>
<p>By adding a @RequestMapping to the Controller, we do all the @RequestMapping of the methods, relative to the controler. It's like subfolders for slugs in the URL:</p>
<p><a target="_blank" rel="noopener noreferrer" href="/moltaweb/cursos/blob/master/images/spring1.png"><img src="/moltaweb/cursos/raw/master/images/spring1.png" alt="@RequestMapping" style="max-width:100%;"></a></p>
<hr>
<h2><a id="user-content-14---spring-mvc---form-tags-and-data-binding" class="anchor" aria-hidden="true" href="#14---spring-mvc---form-tags-and-data-binding"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>14 - SPRING MVC - FORM TAGS AND DATA BINDING</h2>
<h3><a id="user-content-spring-mvc-form-tags-overview" class="anchor" aria-hidden="true" href="#spring-mvc-form-tags-overview"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Spring MVC Form Tags Overview</h3>
<p>Spring Form Tags is a feature of spring that eases development of HTML forms:</p>
<ul>
<li>configurable and reusable for a web page
<ul>
<li>they generate HTML code automatically</li>
</ul>
</li>
<li>can make use of data binding
<ul>
<li>automatically set/retrieve data from Java beans</li>
</ul>
</li>
</ul>
<p>There are many tags available:</p>
<table>
<thead>
<tr>
<th>Form tag</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>form:form</td>
<td>main form container</td>
</tr>
<tr>
<td>form:input</td>
<td>text field</td>
</tr>
<tr>
<td>form:textarea</td>
<td>multi-line text field</td>
</tr>
<tr>
<td>form:checkbox</td>
<td>check box</td>
</tr>
<tr>
<td>form:radiobutton</td>
<td>radio buttons</td>
</tr>
<tr>
<td>form:select</td>
<td>drop down list</td>
</tr>
</tbody>
</table>
<p>More info:<br>
<a href="https://docs.spring.io/spring/docs/5.0.2.RELEASE/spring-framework-reference/web.html#mvc-view-jsp-tags" rel="nofollow">https://docs.spring.io/spring/docs/5.0.2.RELEASE/spring-framework-reference/web.html#mvc-view-jsp-tags</a></p>
<p>we can easily mix the form tags with regular HTML. We only need to add this directive on top of our jsp page:<br>
<code>&lt;%@ taglib prefix="form" uri="http://www.springframework.org/tags/form" %&gt;</code></p>
<p>This is the big picture:</p>
<p><a target="_blank" rel="noopener noreferrer" href="/moltaweb/cursos/blob/master/images/spring2.png"><img src="/moltaweb/cursos/raw/master/images/spring2.png" alt="FormOverview" style="max-width:100%;"></a></p>
<ol>
<li>create Student class with setters/getters for all the properties (First Name, Last Name, etc.)</li>
<li>create a StudentController class with 2 methods</li>
</ol>
<ul>
<li>showForm(Model model)
<ul>
<li>instantiates a student object</li>
<li>we add this object as an attribute to the model -&gt; this bean holds the data binding of the form</li>
<li>returns the student-form.jsp view</li>
</ul>
</li>
</ul>
<div class="highlight highlight-source-java"><pre><span class="pl-k">@RequestMapping</span>(<span class="pl-s"><span class="pl-pds">"</span>/showForm<span class="pl-pds">"</span></span>)
<span class="pl-k">public</span> <span class="pl-smi">String</span> showForm(<span class="pl-smi">Model</span> theModel) {
    theModel<span class="pl-k">.</span>addAttribute(<span class="pl-s"><span class="pl-pds">"</span>student<span class="pl-pds">"</span></span>, <span class="pl-k">new</span> <span class="pl-smi">Student</span>());
    <span class="pl-k">return</span> <span class="pl-s"><span class="pl-pds">"</span>student-form<span class="pl-pds">"</span></span>;
}</pre></div>
<ul>
<li>processForm(@ModelAttribute("student") Student theStudent)
<ul>
<li>we cann pass an annotated argument to make use of the model attribute just created</li>
<li>the object is then populated with the data entered in the form</li>
<li>returns a student-confirmation.jsp page where we can print the data properties from the bean</li>
</ul>
</li>
</ul>
<p><a target="_blank" rel="noopener noreferrer" href="/moltaweb/cursos/blob/master/images/spring3.png"><img src="/moltaweb/cursos/raw/master/images/spring3.png" alt="FormOverview" style="max-width:100%;"></a></p>
<ol start="3">
<li>create student-form.jsp view</li>
</ol>
<ul>
<li>this form contains the Spring Form tags</li>
<li>we create a form aontainer with a modelAttribute, which is the bean instantiated and passed to the model</li>
</ul>
<p><a target="_blank" rel="noopener noreferrer" href="/moltaweb/cursos/blob/master/images/spring4.png"><img src="/moltaweb/cursos/raw/master/images/spring4.png" alt="FormOverview" style="max-width:100%;"></a></p>
<ul>
<li>each tag has a path that corresponds to a propery of the bean (theStudent)
<ul>
<li>when the form is loaded, spring calls getter methods to prepopulate the form (placeholder). If properties have null values, form fields will be empty</li>
<li>when we click submit, spring calls setter methods the object properties are passed to the model so it can be retrieved</li>
</ul>
</li>
</ul>
<ol start="4">
<li>create student-confirmation.jsp</li>
</ol>
<ul>
<li>just to display the data</li>
</ul>
<p><a target="_blank" rel="noopener noreferrer" href="/moltaweb/cursos/blob/master/images/spring5.png"><img src="/moltaweb/cursos/raw/master/images/spring5.png" alt="FormOverview" style="max-width:100%;"></a></p>
<p>Development process</p>
<ol>
<li>Create Student class
<ol>
<li>create properties and getters/setters</li>
</ol>
</li>
<li>Create Student Controller class and form creation code</li>
<li>Create HTML Form
<ol>
<li>add form tags</li>
</ol>
</li>
<li>Create form processing code in the Student Controller class</li>
<li>Create HTML confirmation page
<ol>
<li>add display for data binding</li>
</ol>
</li>
</ol>
<h3><a id="user-content-text-fields" class="anchor" aria-hidden="true" href="#text-fields"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Text Fields</h3>
<p><code>&lt;form:input path="firstName"/&gt;</code></p>
<h3><a id="user-content-drop-down-lists" class="anchor" aria-hidden="true" href="#drop-down-lists"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Drop-down Lists</h3>
<p>This is the actual HTML:</p>
<div class="highlight highlight-text-html-basic"><pre>&lt;<span class="pl-ent">select</span> <span class="pl-e">id</span>=<span class="pl-s"><span class="pl-pds">"</span>country<span class="pl-pds">"</span></span> <span class="pl-e">name</span>=<span class="pl-s"><span class="pl-pds">"</span>country<span class="pl-pds">"</span></span>&gt; 
     &lt;<span class="pl-ent">option</span> <span class="pl-e">value</span>=<span class="pl-s"><span class="pl-pds">"</span>Brazil<span class="pl-pds">"</span></span>&gt;Brazil&lt;/<span class="pl-ent">option</span>&gt; 
     &lt;<span class="pl-ent">option</span> <span class="pl-e">value</span>=<span class="pl-s"><span class="pl-pds">"</span>France<span class="pl-pds">"</span></span>&gt;France&lt;/<span class="pl-ent">option</span>&gt; 
     &lt;<span class="pl-ent">option</span> <span class="pl-e">value</span>=<span class="pl-s"><span class="pl-pds">"</span>Germany<span class="pl-pds">"</span></span>&gt;Germany&lt;/<span class="pl-ent">option</span>&gt; 
     &lt;<span class="pl-ent">option</span> <span class="pl-e">value</span>=<span class="pl-s"><span class="pl-pds">"</span>India<span class="pl-pds">"</span></span>&gt;India&lt;/<span class="pl-ent">option</span>&gt;
&lt;/<span class="pl-ent">select</span>&gt;</pre></div>
<p><strong>Option 1: hardcode options in the JSP file</strong></p>
<p>Add this to the JSP file</p>
<div class="highlight highlight-text-html-basic"><pre>&lt;<span class="pl-ent">form:select</span> <span class="pl-e">path</span>=<span class="pl-s"><span class="pl-pds">"</span>country<span class="pl-pds">"</span></span>&gt;
    &lt;<span class="pl-ent">form:option</span> <span class="pl-e">value</span>=<span class="pl-s"><span class="pl-pds">"</span>Brazil<span class="pl-pds">"</span></span> <span class="pl-e">label</span>=<span class="pl-s"><span class="pl-pds">"</span>Brazil<span class="pl-pds">"</span></span> /&gt;
    &lt;<span class="pl-ent">form:option</span> <span class="pl-e">value</span>=<span class="pl-s"><span class="pl-pds">"</span>France<span class="pl-pds">"</span></span> <span class="pl-e">label</span>=<span class="pl-s"><span class="pl-pds">"</span>France<span class="pl-pds">"</span></span> /&gt;
    &lt;<span class="pl-ent">form:option</span> <span class="pl-e">value</span>=<span class="pl-s"><span class="pl-pds">"</span>Germany<span class="pl-pds">"</span></span> <span class="pl-e">label</span>=<span class="pl-s"><span class="pl-pds">"</span>Germany<span class="pl-pds">"</span></span> /&gt;
    &lt;<span class="pl-ent">form:option</span> <span class="pl-e">value</span>=<span class="pl-s"><span class="pl-pds">"</span>India<span class="pl-pds">"</span></span> <span class="pl-e">label</span>=<span class="pl-s"><span class="pl-pds">"</span>India<span class="pl-pds">"</span></span> /&gt;
&lt;/<span class="pl-ent">form:select</span>&gt;</pre></div>
<p><strong>Option 2: hardcode options in the Student class</strong></p>
<ol>
<li>define country options in the Student class
<ol>
<li>declare a private LinkedHashMap</li>
<li>populate it in the class constructor</li>
<li>create getter for the Map</li>
</ol>
</li>
<li>add this to the JSP file</li>
</ol>
<div class="highlight highlight-text-html-basic"><pre>&lt;<span class="pl-ent">form:select</span> <span class="pl-e">path</span>=<span class="pl-s"><span class="pl-pds">"</span>country<span class="pl-pds">"</span></span>&gt;
    &lt;<span class="pl-ent">form:options</span> <span class="pl-e">items</span>=<span class="pl-s"><span class="pl-pds">"</span>${student.countryOptions}<span class="pl-pds">"</span></span> /&gt;
&lt;/<span class="pl-ent">form:select</span>&gt;</pre></div>
<p><strong>Option 3: Import options from properties file</strong></p>
<p><a href="https://www.udemy.com/spring-hibernate-tutorial/learn/v4/t/lecture/5940154?start=1" rel="nofollow">https://www.udemy.com/spring-hibernate-tutorial/learn/v4/t/lecture/5940154?start=1</a></p>
<p><strong>Option 4: Get options from database dynamically</strong></p>
<p>see later with Hibernate</p>
<h3><a id="user-content-radio-buttons" class="anchor" aria-hidden="true" href="#radio-buttons"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Radio Buttons</h3>
<p>Actual HTML</p>
<div class="highlight highlight-text-html-basic"><pre>Java &lt;<span class="pl-ent">input</span> <span class="pl-e">id</span>=<span class="pl-s"><span class="pl-pds">"</span>favoriteLanguage1<span class="pl-pds">"</span></span> <span class="pl-e">name</span>=<span class="pl-s"><span class="pl-pds">"</span>favoriteLanguage<span class="pl-pds">"</span></span> <span class="pl-e">type</span>=<span class="pl-s"><span class="pl-pds">"</span>radio<span class="pl-pds">"</span></span> <span class="pl-e">value</span>=<span class="pl-s"><span class="pl-pds">"</span>Java<span class="pl-pds">"</span></span>/&gt;
C# &lt;<span class="pl-ent">input</span> <span class="pl-e">id</span>=<span class="pl-s"><span class="pl-pds">"</span>favoriteLanguage2<span class="pl-pds">"</span></span> <span class="pl-e">name</span>=<span class="pl-s"><span class="pl-pds">"</span>favoriteLanguage<span class="pl-pds">"</span></span> <span class="pl-e">type</span>=<span class="pl-s"><span class="pl-pds">"</span>radio<span class="pl-pds">"</span></span> <span class="pl-e">value</span>=<span class="pl-s"><span class="pl-pds">"</span>C#<span class="pl-pds">"</span></span>/&gt;
PHP &lt;<span class="pl-ent">input</span> <span class="pl-e">id</span>=<span class="pl-s"><span class="pl-pds">"</span>favoriteLanguage3<span class="pl-pds">"</span></span> <span class="pl-e">name</span>=<span class="pl-s"><span class="pl-pds">"</span>favoriteLanguage<span class="pl-pds">"</span></span> <span class="pl-e">type</span>=<span class="pl-s"><span class="pl-pds">"</span>radio<span class="pl-pds">"</span></span> <span class="pl-e">value</span>=<span class="pl-s"><span class="pl-pds">"</span>PHP<span class="pl-pds">"</span></span>/&gt;
Python &lt;<span class="pl-ent">input</span> <span class="pl-e">id</span>=<span class="pl-s"><span class="pl-pds">"</span>favoriteLanguage4<span class="pl-pds">"</span></span> <span class="pl-e">name</span>=<span class="pl-s"><span class="pl-pds">"</span>favoriteLanguage<span class="pl-pds">"</span></span> <span class="pl-e">type</span>=<span class="pl-s"><span class="pl-pds">"</span>radio<span class="pl-pds">"</span></span> <span class="pl-e">value</span>=<span class="pl-s"><span class="pl-pds">"</span>Python<span class="pl-pds">"</span></span>/&gt;
Ruby &lt;<span class="pl-ent">input</span> <span class="pl-e">id</span>=<span class="pl-s"><span class="pl-pds">"</span>favoriteLanguage5<span class="pl-pds">"</span></span> <span class="pl-e">name</span>=<span class="pl-s"><span class="pl-pds">"</span>favoriteLanguage<span class="pl-pds">"</span></span> <span class="pl-e">type</span>=<span class="pl-s"><span class="pl-pds">"</span>radio<span class="pl-pds">"</span></span> <span class="pl-e">value</span>=<span class="pl-s"><span class="pl-pds">"</span>Ruby<span class="pl-pds">"</span></span>/&gt;</pre></div>
<p><strong>Option 1: hardcode options in the JSP file</strong></p>
<p>Add this to the JSP file</p>
<div class="highlight highlight-text-html-basic"><pre>Java &lt;<span class="pl-ent">form:radiobutton</span> <span class="pl-e">path</span>=<span class="pl-s"><span class="pl-pds">"</span>favoriteLanguage<span class="pl-pds">"</span></span> <span class="pl-e">value</span>=<span class="pl-s"><span class="pl-pds">"</span>Java<span class="pl-pds">"</span></span> /&gt;
C# &lt;<span class="pl-ent">form:radiobutton</span> <span class="pl-e">path</span>=<span class="pl-s"><span class="pl-pds">"</span>favoriteLanguage<span class="pl-pds">"</span></span> <span class="pl-e">value</span>=<span class="pl-s"><span class="pl-pds">"</span>C#<span class="pl-pds">"</span></span> /&gt;
PHP &lt;<span class="pl-ent">form:radiobutton</span> <span class="pl-e">path</span>=<span class="pl-s"><span class="pl-pds">"</span>favoriteLanguage<span class="pl-pds">"</span></span> <span class="pl-e">value</span>=<span class="pl-s"><span class="pl-pds">"</span>PHP<span class="pl-pds">"</span></span> /&gt;
Python &lt;<span class="pl-ent">form:radiobutton</span> <span class="pl-e">path</span>=<span class="pl-s"><span class="pl-pds">"</span>favoriteLanguage<span class="pl-pds">"</span></span> <span class="pl-e">value</span>=<span class="pl-s"><span class="pl-pds">"</span>Python<span class="pl-pds">"</span></span> /&gt;
Ruby &lt;<span class="pl-ent">form:radiobutton</span> <span class="pl-e">path</span>=<span class="pl-s"><span class="pl-pds">"</span>favoriteLanguage<span class="pl-pds">"</span></span> <span class="pl-e">value</span>=<span class="pl-s"><span class="pl-pds">"</span>Ruby<span class="pl-pds">"</span></span> /&gt;</pre></div>
<p><strong>Option 2: hardcode options in the Student class</strong></p>
<p><a href="https://www.udemy.com/spring-hibernate-tutorial/learn/v4/t/lecture/5820486?start=0" rel="nofollow">https://www.udemy.com/spring-hibernate-tutorial/learn/v4/t/lecture/5820486?start=0</a></p>
<h3><a id="user-content-checkboxes" class="anchor" aria-hidden="true" href="#checkboxes"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Checkboxes</h3>
<p>Similar to Radiobuttons. The difference is that the property in the bean must accept several values --&gt; wen need an ARRAY</p>
<ul>
<li>in the form creation add</li>
</ul>
<div class="highlight highlight-text-html-basic"><pre>Linux &lt;<span class="pl-ent">form:checkbox</span> <span class="pl-e">path</span>=<span class="pl-s"><span class="pl-pds">"</span>operatingSystems<span class="pl-pds">"</span></span> <span class="pl-e">value</span>=<span class="pl-s"><span class="pl-pds">"</span>Linux<span class="pl-pds">"</span></span> /&gt;
MacOS &lt;<span class="pl-ent">form:checkbox</span> <span class="pl-e">path</span>=<span class="pl-s"><span class="pl-pds">"</span>operatingSystems<span class="pl-pds">"</span></span> <span class="pl-e">value</span>=<span class="pl-s"><span class="pl-pds">"</span>MacOS<span class="pl-pds">"</span></span> /&gt;
Windows &lt;<span class="pl-ent">form:checkbox</span> <span class="pl-e">path</span>=<span class="pl-s"><span class="pl-pds">"</span>operatingSystems<span class="pl-pds">"</span></span> <span class="pl-e">value</span>=<span class="pl-s"><span class="pl-pds">"</span>Windows<span class="pl-pds">"</span></span> /&gt;</pre></div>
<ul>
<li>in the Student class, declare operatginSystems as a String[]</li>
<li>in the confirmation form, loop over every possible value:
<ul>
<li>add the tag: &lt;%@ taglib uri="<a href="http://java.sun.com/jsp/jstl/core" rel="nofollow">http://java.sun.com/jsp/jstl/core</a>" prefix="c" %&gt; to provide loop support</li>
<li>add the loop</li>
</ul>
</li>
</ul>
<div class="highlight highlight-text-html-basic"><pre>&lt;<span class="pl-ent">ul</span>&gt;
    &lt;<span class="pl-ent">c:forEach</span> <span class="pl-e">var</span>=<span class="pl-s"><span class="pl-pds">"</span>temp<span class="pl-pds">"</span></span> <span class="pl-e">items</span>=<span class="pl-s"><span class="pl-pds">"</span>${student.operatingSystems}<span class="pl-pds">"</span></span> /&gt;
        &lt;<span class="pl-ent">li</span>&gt;${temp}&lt;/<span class="pl-ent">li</span>&gt;
    &lt;/<span class="pl-ent">c:forEach</span>&gt;
&lt;/<span class="pl-ent">ul</span>&gt;</pre></div>
<hr>
<h2><a id="user-content-15---spring-mvc-form-validation---applying-built-in-validation-rules" class="anchor" aria-hidden="true" href="#15---spring-mvc-form-validation---applying-built-in-validation-rules"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>15 - SPRING MVC FORM VALIDATION - APPLYING BUILT-IN VALIDATION RULES</h2>
<h3><a id="user-content-spring-mvc-form-validation---overview" class="anchor" aria-hidden="true" href="#spring-mvc-form-validation---overview"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Spring MVC Form Validation - Overview</h3>
<p>Check user input from for:</p>
<ul>
<li>required fields</li>
<li>valid numbers in a range</li>
<li>valid format (date, postal code...)</li>
<li>custom rules</li>
<li>etc.</li>
</ul>
<p>Java has a standard API, availabel for server-side or client-side apps (JavaFX, Swing)
Spring supports this API, but needs an implementation (eg Hibernate Validator)</p>
<p>What we'll see:</p>
<ol>
<li>set up dev environment</li>
<li>validate required fields</li>
<li>validate number ranges</li>
<li>validate using regular expression</li>
<li>create custom validation rules</li>
</ol>
<h3><a id="user-content-setting-up-dev-environment-for-form-validation" class="anchor" aria-hidden="true" href="#setting-up-dev-environment-for-form-validation"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Setting up Dev Environment for Form Validation</h3>
<p>We will use Hibernate Validator (there are other options)<br>
<a href="http://hibernate.org/validator/" rel="nofollow">http://hibernate.org/validator/</a></p>
<ol>
<li>Download JAR files from Hibernate website</li>
<li>Add JAR files to the project</li>
</ol>
<p><a target="_blank" rel="noopener noreferrer" href="/moltaweb/cursos/blob/master/images/spring6.png"><img src="/moltaweb/cursos/raw/master/images/spring6.png" alt="Hibernate files" style="max-width:100%;"></a></p>
<h3><a id="user-content-checking-for-required-fields" class="anchor" aria-hidden="true" href="#checking-for-required-fields"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Checking for required fields</h3>
<p>Objective:</p>
<p><a target="_blank" rel="noopener noreferrer" href="/moltaweb/cursos/blob/master/images/spring7.png"><img src="/moltaweb/cursos/raw/master/images/spring7.png" alt="ValidationForm" style="max-width:100%;"></a></p>
<p>In this example, only add validation rule to LastName</p>
<p>Process:</p>
<ol>
<li>add validation rule to Customer class</li>
<li>display error messages in HTML form</li>
<li>perform validation in the Controller class
<ol>
<li>if the validation is not met, it returns to the form</li>
<li>if it's OK, it goes to confirmation page</li>
</ol>
</li>
<li>update confirmation page</li>
</ol>
<p>Step 1:</p>
<p><a target="_blank" rel="noopener noreferrer" href="/moltaweb/cursos/blob/master/images/spring8.png"><img src="/moltaweb/cursos/raw/master/images/spring8.png" alt="Validation1" style="max-width:100%;"></a></p>
<blockquote>
<p>use @NotBlank instead of @NotNull</p>
</blockquote>
<p>Step 2:</p>
<p><a target="_blank" rel="noopener noreferrer" href="/moltaweb/cursos/blob/master/images/spring9.png"><img src="/moltaweb/cursos/raw/master/images/spring9.png" alt="Validation2" style="max-width:100%;"></a></p>
<p>Step 3:</p>
<p><a target="_blank" rel="noopener noreferrer" href="/moltaweb/cursos/blob/master/images/spring10.png"><img src="/moltaweb/cursos/raw/master/images/spring10.png" alt="Validation3" style="max-width:100%;"></a></p>
<p>This is hte important stuff. We add 2 things:</p>
<ul>
<li>@Valid says that the model attribute has to be validated</li>
<li>BindingResult is a container with the results of the validation test</li>
</ul>
<blockquote>
<p><strong>Important</strong>: In the method signature, the BindingResult parameter must immediately after the model attribute.that is being bound</p>
</blockquote>
<p>Step 4:</p>
<p>update the confirmation page:<br>
<code>The student is confirmed: ${student.firstName} ${student.lastName}</code></p>

</article>
  </div>

    </div>

  

  <details class="details-reset details-overlay details-overlay-dark">
    <summary data-hotkey="l" aria-label="Jump to line"></summary>
    <details-dialog class="Box Box--overlay d-flex flex-column anim-fade-in fast linejump" aria-label="Jump to line">
      <!-- '"` --><!-- </textarea></xmp> --></option></form><form class="js-jump-to-line-form Box-body d-flex" action="" accept-charset="UTF-8" method="get"><input name="utf8" type="hidden" value="&#x2713;" />
        <input class="form-control flex-auto mr-3 linejump-input js-jump-to-line-field" type="text" placeholder="Jump to line&hellip;" aria-label="Jump to line" autofocus>
        <button type="submit" class="btn" data-close-dialog>Go</button>
</form>    </details-dialog>
  </details>



  </div>
  <div class="modal-backdrop js-touch-events"></div>
</div>

    </main>
  </div>
  

  </div>

        
<div class="footer container-lg width-full p-responsive" role="contentinfo">
  <div class="position-relative d-flex flex-row-reverse flex-lg-row flex-wrap flex-lg-nowrap flex-justify-center flex-lg-justify-between pt-6 pb-2 mt-6 f6 text-gray border-top border-gray-light ">
    <ul class="list-style-none d-flex flex-wrap col-12 col-lg-6 flex-justify-center flex-lg-justify-start mb-2 mb-lg-0">
      <li class="mr-3">&copy; 2019 <span title="0.68354s from unicorn-6756875f69-grwnj">GitHub</span>, Inc.</li>
        <li class="mr-3"><a data-ga-click="Footer, go to terms, text:terms" href="https://github.com/site/terms">Terms</a></li>
        <li class="mr-3"><a data-ga-click="Footer, go to privacy, text:privacy" href="https://github.com/site/privacy">Privacy</a></li>
        <li class="mr-3"><a data-ga-click="Footer, go to security, text:security" href="https://github.com/security">Security</a></li>
        <li class="mr-3"><a href="https://githubstatus.com/" data-ga-click="Footer, go to status, text:status">Status</a></li>
        <li><a data-ga-click="Footer, go to help, text:help" href="https://help.github.com">Help</a></li>
    </ul>

    <a aria-label="Homepage" title="GitHub" class="footer-octicon mx-lg-4" href="https://github.com">
      <svg height="24" class="octicon octicon-mark-github" viewBox="0 0 16 16" version="1.1" width="24" aria-hidden="true"><path fill-rule="evenodd" d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.013 8.013 0 0 0 16 8c0-4.42-3.58-8-8-8z"/></svg>
</a>
   <ul class="list-style-none d-flex flex-wrap col-12 col-lg-6 flex-justify-center flex-lg-justify-end mb-2 mb-lg-0">
        <li class="mr-3"><a data-ga-click="Footer, go to contact, text:contact" href="https://github.com/contact">Contact GitHub</a></li>
        <li class="mr-3"><a href="https://github.com/pricing" data-ga-click="Footer, go to Pricing, text:Pricing">Pricing</a></li>
      <li class="mr-3"><a href="https://developer.github.com" data-ga-click="Footer, go to api, text:api">API</a></li>
      <li class="mr-3"><a href="https://training.github.com" data-ga-click="Footer, go to training, text:training">Training</a></li>
        <li class="mr-3"><a href="https://github.blog" data-ga-click="Footer, go to blog, text:blog">Blog</a></li>
        <li><a data-ga-click="Footer, go to about, text:about" href="https://github.com/about">About</a></li>

    </ul>
  </div>
  <div class="d-flex flex-justify-center pb-6">
    <span class="f6 text-gray-light"></span>
  </div>
</div>



  <div id="ajax-error-message" class="ajax-error-message flash flash-error">
    <svg class="octicon octicon-alert" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M8.893 1.5c-.183-.31-.52-.5-.887-.5s-.703.19-.886.5L.138 13.499a.98.98 0 0 0 0 1.001c.193.31.53.501.886.501h13.964c.367 0 .704-.19.877-.5a1.03 1.03 0 0 0 .01-1.002L8.893 1.5zm.133 11.497H6.987v-2.003h2.039v2.003zm0-3.004H6.987V5.987h2.039v4.006z"/></svg>
    <button type="button" class="flash-close js-ajax-error-dismiss" aria-label="Dismiss error">
      <svg class="octicon octicon-x" viewBox="0 0 12 16" version="1.1" width="12" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.48 8l3.75 3.75-1.48 1.48L6 9.48l-3.75 3.75-1.48-1.48L4.52 8 .77 4.25l1.48-1.48L6 6.52l3.75-3.75 1.48 1.48L7.48 8z"/></svg>
    </button>
    You can’t perform that action at this time.
  </div>


    
    <script crossorigin="anonymous" integrity="sha512-NrjCh49VLw2768XCSxbHHsu05NjXH1bEbBxduYC8V1OW7L9fK7jF2OrX3dyplx4IwphXOPSbTAd8zuqHBGN59g==" type="application/javascript" src="https://github.githubassets.com/assets/frameworks-40c99db0.js"></script>
    
    <script crossorigin="anonymous" async="async" integrity="sha512-yiZTcqz3N5CvEb6a0EFnmq0O07Ut/9u/K72Jiwv9i6H0gT47XuLcUpL+HCgctmKkua1VVfqMbPEAGW8bNCM1sg==" type="application/javascript" src="https://github.githubassets.com/assets/github-bootstrap-f71ca13d.js"></script>
    
    
    
  <div class="js-stale-session-flash stale-session-flash flash flash-warn flash-banner" hidden
    >
    <svg class="octicon octicon-alert" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M8.893 1.5c-.183-.31-.52-.5-.887-.5s-.703.19-.886.5L.138 13.499a.98.98 0 0 0 0 1.001c.193.31.53.501.886.501h13.964c.367 0 .704-.19.877-.5a1.03 1.03 0 0 0 .01-1.002L8.893 1.5zm.133 11.497H6.987v-2.003h2.039v2.003zm0-3.004H6.987V5.987h2.039v4.006z"/></svg>
    <span class="signed-in-tab-flash">You signed in with another tab or window. <a href="">Reload</a> to refresh your session.</span>
    <span class="signed-out-tab-flash">You signed out in another tab or window. <a href="">Reload</a> to refresh your session.</span>
  </div>
  <template id="site-details-dialog">
  <details class="details-reset details-overlay details-overlay-dark lh-default text-gray-dark" open>
    <summary aria-haspopup="dialog" aria-label="Close dialog"></summary>
    <details-dialog class="Box Box--overlay d-flex flex-column anim-fade-in fast">
      <button class="Box-btn-octicon m-0 btn-octicon position-absolute right-0 top-0" type="button" aria-label="Close dialog" data-close-dialog>
        <svg class="octicon octicon-x" viewBox="0 0 12 16" version="1.1" width="12" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.48 8l3.75 3.75-1.48 1.48L6 9.48l-3.75 3.75-1.48-1.48L4.52 8 .77 4.25l1.48-1.48L6 6.52l3.75-3.75 1.48 1.48L7.48 8z"/></svg>
      </button>
      <div class="octocat-spinner my-6 js-details-dialog-spinner"></div>
    </details-dialog>
  </details>
</template>

  <div class="Popover js-hovercard-content position-absolute" style="display: none; outline: none;" tabindex="0">
  <div class="Popover-message Popover-message--bottom-left Popover-message--large Box box-shadow-large" style="width:360px;">
  </div>
</div>

  <div aria-live="polite" class="js-global-screen-reader-notice sr-only"></div>

  </body>
</html>

