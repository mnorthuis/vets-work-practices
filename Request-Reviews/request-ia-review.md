# Information Architecture

* **This document applies only to External Contractors.**

* **Definitions for terms used in this folder:**

  * *"DSVA" refers to DSVA team members and DSVA detailees.*

  * *"Internal contractors" refers to DSVA's primary vendor contractor and its subcontractors.*

  * *"External contractors" refers to any other contractor team working on the Veteran-facing Services Platform.*

<hr>

* [General](#general)
* [Prepare for an IA review](#prepare-for-an-ia-review)
* [Request an IA review](#request-an-ia-review)

<hr>

### General

* **All teams working on the Veteran-facing Services Platform are required to work with DSVA to integrate your service into the platform so your users can easily find (and search for) your service.**
* **External Contractor teams should intiate the IA review as soon as they have a good idea of what their service will do.** 
  * For most teams, this will be at some point in the *Prototype* phase or early in the *Build and Test* phase. 

<hr>

## Prepare for an IA Review

### Step 1: Define the service name

*If you're building on to an existing service, you can skip this step.*

If you're building a new service, you'll need to create a name for it.

* Be sure to test the service name with your users.


### Step 2: Define the Information Architecture

The IA determines where in the Veteran-facing Services Platform your service will live, how users navigate to your service, and how users navigate within your service. 

* How your service will integrate into the existing Veteran-facing Services Platform?
  * Is this a new standalone service, or is it part of an existing service?
  * Does the service require authentication? 
  * If yes, will there be static content available prior to authentication? Currently we build static content pages for tools that require authentication to provide SEO value and a landing page in the user experience rather than an immediate redirect to login when accessing. 

* How will your users find and get to your service?
  * Consider top navigation, home page, hub pages, and crosslinking opportunities
  * Top nav and Top Tasks on the home page are limited to the top key tasks of a benefit area
  * Hub pages are limited to 10 links per spoke (Get, Manage and More), and 5 links in the Other Benefits section

* Where does your service live within the existing content hubs?
  * Which directory (or subdirectory) does it live in?

* Will the service live in the global navigation of the site? 
  * If so, where?
  * If not, how will users navigate to your service?

* What are the primary entry points to the service?

* Would cross-linking from other tools on the Veteran-facing Services Platform help Veterans find and use your service?
  * If so, what are those secondary entry points?

* What is the ```<h1>``` (the page title) for each page/screen of your service?
  * Inputs to decision are SEO and user terminology, internal VA terms, Form #s


### Step 3: Define the URLs

As part of defining the information architecture in [Step #2](#step-2-define-the-information-architecture), you identified the directory (or subdirectory) in which your service will live. For example, in the ```health-care/apply-for-health-care-form-10-10ez/``` directory.

You also defined the ```<h1>``` page titles for each page or screen. For example, ```veteran-information/personal-information``` and ```veteran-information/birth-information```.

Now you can define the URL(s) for your service by putting those two elements together. For example, ```health-care/apply-for-health-care-form-10-10ez/veteran-information```.


#### Guidelines for creating URLs

* Keep directory and page URLs as short as possible, without losing their meaning.

* URLs should be all lowercase.

* Use hyphens; don't use underscores (or white space). Underscoring can change two words into one word, for example, "health care" becomes "healthcare."

* Use the ```<h1>``` page title as your guide, but you do not need to match it exactly.

* Use the most descriptive of all the keywords used on the page. Include only keywords that help the reader understand the point of the page.

* Do not load or repeat keywords in the URL &mdash; search engines will pick up other keywords from other elements on the page.

* Don't include words that don't add meaning, such as "the" or "a."

* Avoid repetition of words. In some cases it may naturally happen, but avoid it when possible.

* For form URLs, use the form number, as well as keywords that describe the purpose of the form:

  * **structure**
    <code>/action-keyword1-keywordn-form-number/</code>

  * **example** *(page is not live)*
    <code>https://www.va.gov/pension/apply-for-veteran-pension-form-527ez</code>  

* For tool URLs, use an action word and keywords to describe the tool:

  * **structure**
    <code>/action-keyword1-keywordn/</code>

  * **example** *(page is not live)* 
    <code>https://www.va.gov/health-care/refill-track-prescriptions</code>  
  
* Some tools are merely reporting and do not require an action on the part of the user, and therefore may not have an action word in their URL.  

  * **example:** *(page is not live)* 
  * <code>https://www.va.gov/claim-or-appeal-status/</code>.  Use SEO and IA structure as guidance. 
 
* If a tool/form requires authentication and will have static page available to unauthenticated users, ensure that URL for that static page is optimized for SEO and UX.  The URL for the actual tool/form behind authentication can be less descriptive.  

  * **example** *(page is not live)*
  * static page: <code>https://www.va.gov/claim-or-appeal-status/</code>
  * tool/form:  <code>https://www.va.gov/claim-or-appeal-status/status/</code>
    
### Step 4: Test the proposed Information Architecture with Veterans

* Your service's IA should map to Veteran mental models &mdash; even if this differs from how VA thinks about your service.

* Use card sorting, tree testing, or user interviews to test the information architecture you defined in [Step #2](#step-2-define-the-information-architecture) and  the URLs you defined in [Step #3](#step-3-define-the-urls).


### Step 5: Define meta page description

Define the page meta description for each page/screen in your service.

* Keep the description short: 1-2 sentences.
* Describe the most important thing the Veteran can do on the page/screen. For example, <a href="https://www.vets.gov/health-care/after-you-apply/" target="_blank">on the ```After you apply``` page</a>, the meta description is ```Find out what to do after applying for VA health care benefits, including when to schedule your first VA medical appointment```.


<hr>

## Request an IA Review

1. File an issue in ```vets-team repo```.
    * Title: ```Request IA Review```
    * Labels: 
      * ```ia```
      * ```external-request```
      * ```[your team's Github label]```, e.g., "BAH-526"
    * Assign the issue to: ```[your DSVA contact]```
    * Comment: Include the following information. For each item, include a summary of any user testing you did that led to your choice.
      * **Service name** (if creating a new service): ```the name of your service```
      * **Information Architecture**: ```Upload a diagram or table illustrating how users navigate to your service and from where```
      * **Page Title/URL/Page meta description**: ```a table showing each Page Title, its URL, and its Meta Description```
1. **Within 4 business days**, DSVA will conduct an IA Review and provide feedback.
    * If you don't hear anything after 4 business days, reach out to your DSVA Contact.
    * DSVA's goal in this review is to make sure your service doesn’t collide with existing services and to provide feedback based on Veteran experiences with other Veteran-facing Services Platform services.
1. DSVA will update the Github issue with a Word document that provides feedback and any requested changes.
1. Complete all the changes requested in the Word document.
    * If your team has questions (or disagrees with a requested change), use the Github issue to discuss that with DSVA.
1. When all changes are completed, close the issue.
1. When the issue is closed, this pre-launch activity is considered complete.
