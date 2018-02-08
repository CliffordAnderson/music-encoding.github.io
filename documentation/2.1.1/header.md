---
layout: oldGuidelines
---
<div xmlns="http://www.w3.org/1999/xhtml">
   <article class="page type-page status-publish hentry">
      <div class="entry-content">
         <div class="panel-grid">
            <div class="panel-grid-cell" style="width: 65%; float: left;">
               <div class="panel widget widget_text panel-first-child panel-last-child">
                  <div class="textwidget">
                     <section class="div1" id="header">
                        <header>
                           <h1><span class="headingNumber">2 </span><span class="head">The MEI
                                 Header</span></h1>
                        </header>
                        <p>This chapter addresses the description of an encoded
                           item so that the musical text, as well as its sources, encoding, and revisions are
                           all
                           thoroughly documented. Such documentation is necessary for scholars using the texts,
                           for
                           software processing them, and for catalogers in libraries and archives. Together these
                           descriptions and declarations provide an electronic analog to the title page attached
                           to a
                           printed work. They also constitute an equivalent for the content of the code books
                           or
                           introductory manuals customarily accompanying electronic data sets.
                        </p>
                        <p>Every
                           MEI-conformant text not embedded in another XML carrier that provides for capturing
                           metadata, such as TEI or METS, must carry a set of descriptions, prefixed to it and
                           encoded as described in this chapter. This set is known as the MEI header, tagged
                           <a class="link_odd_elementSpec" href="/documentation/2.1.1/meiHead">meiHead</a>, and has five major parts:
                        </p>
                        <ol>
                           
                           <li class="item">one or more alternative identifiers, tagged with <a class="link_odd_elementSpec" href="/documentation/2.1.1/altId">altId</a>, each of which provides an identifying name or number associated
                              with the file.
                           </li>
                           
                           <li class="item">a <span class="term">file description</span>, tagged <a class="link_odd_elementSpec" href="/documentation/2.1.1/fileDesc">fileDesc</a>, containing a full bibliographic description of the computer
                              file itself, from which a user of the text could derive a proper bibliographic citation,
                              or which a librarian or archivist could use in creating a catalog entry recording
                              its
                              presence within a library or archive. The term <span class="term">computer file</span>
                              here is to be understood as referring to the whole intellectual entity or document
                              described by the header, even when this is stored in multiple physical operating system
                              files. The file description also includes information about the source or sources
                              from
                              which the electronic document was derived. The MEI elements used to encode the file
                              description are described in section <a class="link_ptr" href="/documentation/2.1.1/header#fileDescription" title="File Description"><span class="headingNumber">2.1 </span>File Description</a>
                              below.
                           </li>
                           
                           <li class="item">an <span class="term">encoding description</span>, tagged <a class="link_odd_elementSpec" href="/documentation/2.1.1/encodingDesc">encodingDesc</a>, which describes the relationship between an
                              electronic text and its source or sources. It allows for detailed description of whether
                              (or how) the text was normalized during transcription, how the encoder resolved
                              ambiguities in the source, what levels of encoding or analysis were applied, and similar
                              matters. The MEI elements used to encode the encoding description are described in
                              section <a class="link_ptr" href="/documentation/2.1.1/header#encodingDescription" title="Encoding Description"><span class="headingNumber">2.2 </span>Encoding Description</a> below.
                           </li>
                           
                           <li class="item">a <span class="term">work description</span>, tagged <a class="link_odd_elementSpec" href="/documentation/2.1.1/workDesc">workDesc</a>, containing classification and contextual information about
                              the work, such as its subject matter, the situation in which it was produced, the
                              individuals described by or participating in producing it, and so forth. Such a work
                              profile is of particular use in highly structured composite texts such as corpora
                              or
                              language collections, where it is often highly desirable to enforce a controlled
                              descriptive vocabulary or to perform retrievals from a body of text in terms of text
                              type or origin. The work description may however be of use in any form of automatic
                              text
                              processing. The MEI elements used to encode the <span class="term">work
                                 description</span> are described in section <a class="link_ptr" href="/documentation/2.1.1/header#workDescription" title="Work Description"><span class="headingNumber">2.3
                                    </span>Work Description</a> below.
                           </li>
                           
                           <li class="item">a <span class="term">revision history</span>, tagged <a class="link_odd_elementSpec" href="/documentation/2.1.1/revisionDesc">revisionDesc</a>, which allows the encoder to provide a history of changes
                              made during the development of the electronic text. The revision history is important
                              for <span class="term">version control</span> and for resolving questions about the
                              history of a file. The MEI elements used to encode the revision description are
                              described in section <a class="link_ptr" href="/documentation/2.1.1/header#revisionDescription" title="Revision Description"><span class="headingNumber">2.4 </span>Revision
                                 Description</a> below.
                           </li>
                           
                        </ol>
                        <div class="div2" id="fileDescription">
                           <h2><span class="headingNumber">2.1 </span><span class="head">File Description</span></h2>
                           <p>The structure of the bibliographic
                              description of a machine-readable or digital musical text resembles that of a book,
                              an
                              article, or other kinds of textual objects. The file description element of the MEI
                              header has therefore been closely modelled on existing standards in library cataloging;
                              it should thus provide enough information to allow users to give standard bibliographic
                              references to the electronic text, and to allow catalogers to catalog it. Bibliographic
                              citations occurring elsewhere in the header, and in the text itself, are derived from
                              the same model.
                           </p>
                           <p>The bibliographic description of an electronic musical text should
                              be supplied by the mandatory <a class="link_odd_elementSpec" href="/documentation/2.1.1/fileDesc">fileDesc</a> element:
                           </p>
                           <ul class="specList">
                              
                              <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/fileDesc">fileDesc</a></span> (file
                                 description) – Contains a full bibliographic description of the MEI file.
                              </li>
                              
                           </ul>
                           <p>The <a class="link_odd_elementSpec" href="/documentation/2.1.1/fileDesc">fileDesc</a> element contains two mandatory and
                              six optional elements, each of which is described in more detail below. These elements
                              are listed below in the order in which they must occur within the <a class="link_odd_elementSpec" href="/documentation/2.1.1/fileDesc">fileDesc</a> element.
                           </p>
                           <ul class="specList">
                              
                              <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/titleStmt">titleStmt</a></span> (title
                                 statement) – Container for title and responsibility meta-data.
                              </li>
                              
                              <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/editionStmt">editionStmt</a></span>
                                 (edition statement) – Container for meta-data pertaining to a particular edition of
                                 the material being described.
                              </li>
                              
                              <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/extent">extent</a></span> Used to
                                 express size in terms other than physical dimensions, such as number of pages, number
                                 of records in file, number of bytes, performance duration for music, audio recordings
                                 and visual projections, etc.
                              </li>
                              
                              <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/pubStmt">pubStmt</a></span>
                                 (publication statement) – Container for information regarding the publication or
                                 distribution of a bibliographic item, including the publisher's name and address,
                                 the
                                 date of publication, and other relevant details.
                              </li>
                              
                              <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/seriesStmt">seriesStmt</a></span>
                                 (series statement) – Groups information about the series, if any, to which a
                                 publication belongs.
                              </li>
                              
                              <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/notesStmt">notesStmt</a></span> (notes
                                 statement)– Collects any notes providing information about a text additional to that
                                 recorded in other parts of the bibliographic description.
                              </li>
                              
                              <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/sourceDesc">sourceDesc</a></span>
                                 (source description) – A container for the descriptions of the source(s) used in the
                                 creation of the electronic file.
                              </li>
                              
                           </ul>
                           <p>A complete file description will resemble the following example:</p>
                           <div id="index.xml-egXML-d39e2177" class="pre egXML_valid">
                              <span data-indentation="1" class="element">&lt;fileDesc&gt;</span><br />   <span data-indentation="2" class="element">&lt;titleStmt&gt;</span><br />     <span data-indentation="3" class="element">&lt;title/&gt;</span><br />   <span data-indentation="2" class="element">&lt;/titleStmt&gt;</span><br />   <span data-indentation="2" class="element">&lt;editionStmt&gt;</span><br />        <span data-indentation="2" class="element">&lt;/editionStmt&gt;</span><br />
                                <span data-indentation="2" class="element">&lt;extent/&gt;</span><br />   <span data-indentation="2" class="element">&lt;pubStmt&gt;</span><br />        <span data-indentation="2" class="element">&lt;/pubStmt&gt;</span><br />   <span data-indentation="2" class="element">&lt;seriesStmt&gt;</span><br />        <span data-indentation="2" class="element">&lt;/seriesStmt&gt;</span><br />   <span data-indentation="2" class="element">&lt;notesStmt&gt;</span><br />     <span data-indentation="3" class="element">&lt;annot/&gt;</span><br />   <span data-indentation="2" class="element">&lt;/notesStmt&gt;</span><br />   <span data-indentation="2" class="element">&lt;sourceDesc&gt;</span><br />     
                                <span data-indentation="2" class="element">&lt;/sourceDesc&gt;</span><br />
                              <span data-indentation="1" class="element">&lt;/fileDesc&gt;</span>
                              
                           </div>
                           <div class="div3" id="titlestmt">
                              <h3><span class="headingNumber">2.1.1 </span><span class="head">Title Statement</span></h3>
                              <p>The <a class="link_odd_elementSpec" href="/documentation/2.1.1/titleStmt">titleStmt</a> element is the first component of the <a class="link_odd_elementSpec" href="/documentation/2.1.1/fileDesc">fileDesc</a> element, and is mandatory:
                              </p>
                              <ul class="specList">
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/titleStmt">titleStmt</a></span>
                                    (title statement) – Container for title and responsibility meta-data.
                                 </li>
                                 
                              </ul>
                              <p>The title statement contains the title given to the electronic work, together
                                 with one or more optional statements of responsibility which identify the encoder,
                                 editor, author, compiler, or other parties responsible for it:
                              </p>
                              <ul class="specList">
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/title">title</a></span> Title of a
                                    bibliographic entity.
                                 </li>
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/arranger">arranger</a></span> A
                                    person or organization who transcribes a musical composition, usually for a
                                    different medium from that of the original; in an arrangement the musical substance
                                    remains essentially unchanged.
                                 </li>
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/author">author</a></span> The name of
                                    the creator of the intellectual content of a non-musical, literary work.
                                 </li>
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/composer">composer</a></span> The
                                    name of the creator of the intellectual content of a musical work.
                                 </li>
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/editor">editor</a></span> The name of
                                    the individual(s), institution(s) or organization(s) acting in an editorial
                                    capacity.
                                 </li>
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/funder">funder</a></span> Names of
                                    individuals, institutions, or organizations responsible for funding. Funders provide
                                    financial support for a project; they are distinct from sponsors, who provide
                                    intellectual support and authority.
                                 </li>
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/librettist">librettist</a></span>
                                    Person or organization who is a writer of the text of an opera, oratorio, etc.
                                 </li>
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/lyricist">lyricist</a></span> Person
                                    or organization who is a writer of the text of a song.
                                 </li>
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/sponsor">sponsor</a></span> Names of
                                    sponsoring individuals, organizations or institutions. Sponsors give their
                                    intellectual authority to a project; they are to be distinguished from funders, who
                                    provide the funding but do not necessarily take intellectual responsibility.
                                 </li>
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/respStmt">respStmt</a></span>
                                    (responsibility statement) – Names one or more individuals, groups, or in rare
                                    cases, mechanical processes, responsible for creation or realization of the
                                    intellectual or artistic content.
                                 </li>
                                 
                              </ul>
                              <p>The <a class="link_odd_elementSpec" href="/documentation/2.1.1/title">title</a> element contains the chief name of the
                                 electronic work. Its content takes the form considered appropriate by its creator.
                                 The
                                 element may be repeated, if the work has more than one title (perhaps in different
                                 languages). Where the electronic work is derived from an existing source text, it
                                 is
                                 strongly recommended that the title for the former should be derived from the latter,
                                 but clearly distinguishable from it, for example by the addition of a phrase such
                                 as
                                 ‘: an electronic transcription’ or ‘a digital edition’. This will distinguish the
                                 electronic work from the source text in citations and in catalogs, which contain
                                 descriptions of both types of material.
                              </p>
                              <div id="index.xml-egXML-d39e2244" class="pre egXML_valid">
                                 <span data-indentation="1" class="element">&lt;titleStmt
                                    xmlns="http://www.music-encoding.org/ns/mei"&gt;</span><br />   <span data-indentation="2" class="element">&lt;title&gt;</span>Lieder-Album für die Jugend <span data-indentation="2" class="element">&lt;/title&gt;</span><br />   <span data-indentation="2" class="element">&lt;title <span class="attribute">type</span>="<span class="attributevalue">subtitle</span>"&gt;</span><br />für Singstimme(n) und Klavier, <span data-indentation="3" class="element">&lt;identifier&gt;</span>op.     79<span data-indentation="3" class="element">&lt;/identifier&gt;</span><br /><span data-indentation="2" class="element">&lt;/title&gt;</span><br />   <span data-indentation="2" class="element">&lt;title <span class="attribute">type</span>="<span class="attributevalue">subtitle</span>"&gt;</span>an electronic transcription<span data-indentation="2" class="element">&lt;/title&gt;</span><br />
                                 <span data-indentation="1" class="element">&lt;/titleStmt&gt;</span>
                                 
                              </div>
                              <p>Other alternative titles or subtitles may be encoded in additional title
                                 elements with values in the <span class="att">type</span> attribute that distinguish
                                 them from the chief title. Sample values for the <span class="att">type</span>
                                 attribute include: main (main title), subordinate (subtitle, title of part),
                                 abbreviated (abbreviated form of title), alternative (alternate title by which the
                                 work is also known), translated (translated form of title), uniform (collective
                                 title).
                              </p>
                              <p>The <span class="att">type</span> attribute is provided for convenience
                                 in analyzing titles and processing them according to their type; where such
                                 specialized processing is not necessary, there is no need for such analysis, and the
                                 entire title, including subtitles and any parallel titles, may be enclosed within
                                 a
                                 single <a class="link_odd_elementSpec" href="/documentation/2.1.1/title">title</a> element, as in the following
                                 example:
                              </p>
                              <div id="index.xml-egXML-d39e2276" class="pre egXML_valid">
                                 <span data-indentation="1" class="element">&lt;title&gt;</span>Symphony No. 5 in C Minor : an electronic transcription<span data-indentation="1" class="element">&lt;/title&gt;</span>
                                 
                              </div>
                              <p>The electronic work will also have an external name (its ‘filename’ or ‘data
                                 set name’) or reference number on the computer system where it resides at any time.
                                 This name is likely to change frequently, as new copies of the file are made on the
                                 computer system. Its form is entirely dependent on the particular computer system
                                 in
                                 use and thus cannot always easily be transferred from one system to another. Moreover,
                                 a given work may be composed of many files. For these reasons, these Guidelines
                                 strongly recommend that such names should not be used as the title for any electronic
                                 work.
                              </p>
                              <p>Helpful guidance on the formulation of useful descriptive titles in
                                 difficult cases may be found in the Anglo-American Cataloguing Rules (Gorman and
                                 Winkler, 1978, chapter 25) or in equivalent national-level bibliographical
                                 documentation.
                              </p>
                              <p>At a minimum, the creator of the musical text and the creator of
                                 the file should be identified. If the bibliographic description is for a corpus,
                                 identify the creator of the corpus. Optionally also include the names of others
                                 involved in the transcription or elaboration of the text, sponsors, and funding
                                 agencies. The name of the person responsible for physical data input need not normally
                                 be recorded, unless that person is also intellectually responsible for some aspect
                                 of
                                 the creation of the file.
                              </p>
                              <p>In traditional bibliographic practice, those with
                                 primary creative responsibility are given special prominence. MEI accommodates this
                                 approach by providing responsibility-role elements. For example:
                              </p>
                              <div id="index.xml-egXML-d39e2290" class="pre egXML_valid">
                                 <span data-indentation="1" class="element">&lt;titleStmt&gt;</span><br />   <span data-indentation="2" class="element">&lt;title&gt;</span>Auf dem Hügel sitz ich spähend : an electronic transcription<span data-indentation="2" class="element">&lt;/title&gt;</span><br />   <span data-indentation="2" class="element">&lt;composer&gt;</span>Ludwig van Beethoven<span data-indentation="2" class="element">&lt;/composer&gt;</span><br />   <span data-indentation="2" class="element">&lt;lyricist&gt;</span>Aloys Jeitteles<span data-indentation="2" class="element">&lt;/lyricist&gt;</span><br />
                                 <span data-indentation="1" class="element">&lt;/titleStmt&gt;</span>
                                 
                              </div>
                              <p>Secondary intellectual responsibility in this case is encoded using <a class="link_odd_elementSpec" href="/documentation/2.1.1/respStmt">respStmt</a>. The <a class="link_odd_elementSpec" href="/documentation/2.1.1/respStmt">respStmt</a>
                                 element has two subcomponents: a <a class="link_odd_elementSpec" href="/documentation/2.1.1/name">name</a> element
                                 identifying a responsible individual or organization, and a <a class="link_odd_elementSpec" href="/documentation/2.1.1/resp">resp</a> element indicating the nature of the responsibility. All names
                                 should be stated in the form in which the persons or bodies wish to be publicly cited.
                                 This will usually be the fullest form of the name, including first names. No specific
                                 recommendations are made at this time as to appropriate content for <a class="link_odd_elementSpec" href="/documentation/2.1.1/resp">resp</a>. However, it should make clear the nature of the
                                 responsibility.
                              </p>
                              <div id="index.xml-egXML-d39e2321" class="pre egXML_valid">
                                 <span data-indentation="1" class="element">&lt;titleStmt&gt;</span><br />   <span data-indentation="2" class="element">&lt;title&gt;</span>Auf dem Hügel sitz ich spähend : an electronic transcription<span data-indentation="2" class="element">&lt;/title&gt;</span><br />   <span data-indentation="2" class="element">&lt;composer&gt;</span>Ludwig van Beethoven<span data-indentation="2" class="element">&lt;/composer&gt;</span><br />   <span data-indentation="2" class="element">&lt;lyricist&gt;</span>Aloys Jeitteles<span data-indentation="2" class="element">&lt;/lyricist&gt;</span><br />   <span data-indentation="2" class="element">&lt;respStmt&gt;</span><br />     <span data-indentation="3" class="element">&lt;resp&gt;</span>Encoded by<span data-indentation="3" class="element">&lt;/resp&gt;</span><br />     <span data-indentation="3" class="element">&lt;name&gt;</span>Maja Hartwig<span data-indentation="3" class="element">&lt;/name&gt;</span><br />     <span data-indentation="3" class="element">&lt;name&gt;</span>Kristina Richts<span data-indentation="3" class="element">&lt;/name&gt;</span><br />
                                   <span data-indentation="2" class="element">&lt;/respStmt&gt;</span><br />
                                 <span data-indentation="1" class="element">&lt;/titleStmt&gt;</span>
                                 
                              </div>
                              <p>This method of encoding facilitates exchange of bibliographic data with library
                                 catalogs and bibliographic databases as well as applications whose handling of
                                 bibliographic data is restricted to traditional responsibility roles. Additional
                                 information regarding these responsibility-role elements can be found in chapter <a class="link_ptr" href="/documentation/2.1.1/shared#bibliographicCitations" title="Bibliographic Citations and References"><span class="headingNumber">1.3.6
                                       </span>Bibliographic Citations and References</a>.
                              </p>
                              <p>When the MEI.namesdates
                                 module is enabled, two additional elements are also permitted within <a class="link_odd_elementSpec" href="/documentation/2.1.1/respStmt">respStmt</a>:
                              </p>
                              <ul class="specList">
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/corpName">corpName</a></span>
                                    (corporate name) – Identifies an organization or group of people that acts as a
                                    single entity.
                                 </li>
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/persName">persName</a></span>
                                    (personal name) – Designation for an individual, including any or all of that
                                    individual's forenames, surnames, honorific titles, and added names.
                                 </li>
                                 
                              </ul>
                              <p>These elements allow for more precise identification of the entity associated
                                 with the name than is permitted by the simpler <a class="link_odd_elementSpec" href="/documentation/2.1.1/name">name</a>
                                 element. The following example shows how a precise date range can be associated with
                                 a
                                 personal or corporate name.
                              </p>
                              <div id="index.xml-egXML-d39e2367" class="pre egXML_valid">
                                 <span data-indentation="1" class="element">&lt;respStmt&gt;</span><br />   <span data-indentation="2" class="element">&lt;resp&gt;</span>Machine-readable transcription by: <span data-indentation="2" class="element">&lt;/resp&gt;</span><br />   <span data-indentation="2" class="element">&lt;persName <span class="attribute">enddate</span>="<span class="attributevalue">1940-11-06</span>" <span class="attribute">startdate</span>="<span class="attributevalue">1860-01-01</span>"&gt;</span>John Doe<span data-indentation="2" class="element">&lt;/persName&gt;</span><br />
                                 <span data-indentation="1" class="element">&lt;/respStmt&gt;</span>
                                 
                              </div>
                              <p>For additional information about corporate and personal names, see chapter <a class="link_ptr" href="/documentation/2.1.1/namesDates" title="0"><span class="headingNumber">18
                                       </span>Names and Dates</a>.
                              </p>
                              <p>In addition to, or instead of the <a class="link_odd_elementSpec" href="/documentation/2.1.1/resp">resp</a> element, the <span class="att">role</span> attribute on <a class="link_odd_elementSpec" href="/documentation/2.1.1/name">name</a>, <a class="link_odd_elementSpec" href="/documentation/2.1.1/persName">persName</a>, and <a class="link_odd_elementSpec" href="/documentation/2.1.1/corpName">corpName</a> may be used to capture the nature of
                                 responsibility. While <a class="link_odd_elementSpec" href="/documentation/2.1.1/resp">resp</a> accommodates capturing the
                                 wide variety of text that may occur in responsibility statements, use of the <span class="att">role</span> attribute provides the possibility of recording a controlled
                                 value independently of the textual content of <a class="link_odd_elementSpec" href="/documentation/2.1.1/resp">resp</a>.
                              </p>
                              <div id="index.xml-egXML-d39e2410" class="pre egXML_valid">
                                 <span data-indentation="1" class="element">&lt;respStmt&gt;</span><br />   <span data-indentation="2" class="element">&lt;resp&gt;</span>Encoded by <span data-indentation="2" class="element">&lt;/resp&gt;</span><br />   <span data-indentation="2" class="element">&lt;corpName <span class="attribute">role</span>="<span class="attributevalue">encoder</span>"&gt;</span>Members of the Local Symphony Orchestra<span data-indentation="2" class="element">&lt;/corpName&gt;</span><br />
                                 <span data-indentation="1" class="element">&lt;/respStmt&gt;</span>
                                 
                              </div>
                              <p>Values from the MARC relator code list (<a class="link_ref" href="http://www.loc.gov/marc/relators/relacode.html">http://www.loc.gov/marc/relators/relacode.html</a>) or term list (<a class="link_ref" href="http://www.loc.gov/marc/relators/relaterm.html">http://www.loc.gov/marc/relators/relaterm.html</a>) are recommended for <span class="att">role</span>, where applicable.
                              </p>
                              <p>Where it is necessary to group
                                 responsibilities and names, multiple responsibility statements may be used. For
                                 example:
                              </p>
                              <div id="index.xml-egXML-d39e2434" class="pre egXML_valid">
                                 <span data-indentation="1" class="element">&lt;titleStmt&gt;</span><br />   <span data-indentation="2" class="element">&lt;title&gt;</span>Symphony No. 5 in C Minor : an electronic transcription<span data-indentation="2" class="element">&lt;/title&gt;</span><br />   <span data-indentation="2" class="element">&lt;respStmt&gt;</span><br />     <span data-indentation="3" class="element">&lt;resp&gt;</span>Encoded by<span data-indentation="3" class="element">&lt;/resp&gt;</span><br />     <span data-indentation="3" class="element">&lt;persName <span class="attribute">role</span>="<span class="attributevalue">encoder</span>"&gt;</span>Joe Encoder<span data-indentation="3" class="element">&lt;/persName&gt;</span><br />     <span data-indentation="3" class="element">&lt;persName <span class="attribute">role</span>="<span class="attributevalue">encoder</span>"&gt;</span>Jane Decoder<span data-indentation="3" class="element">&lt;/persName&gt;</span><br />   <span data-indentation="2" class="element">&lt;/respStmt&gt;</span><br />   <span data-indentation="2" class="element">&lt;respStmt&gt;</span><br />     <span data-indentation="3" class="element">&lt;resp&gt;</span>Images scanned by<span data-indentation="3" class="element">&lt;/resp&gt;</span><br />
                                     <span data-indentation="3" class="element">&lt;persName&gt;</span>Ludwig van Ludwig<span data-indentation="3" class="element">&lt;/persName&gt;</span><br />   <span data-indentation="2" class="element">&lt;/respStmt&gt;</span><br />
                                 <span data-indentation="1" class="element">&lt;/titleStmt&gt;</span>
                                 
                              </div>
                              <p>It is often desirable to mix primary and secondary intellectual responsibility
                                 information. Treating all intellectual roles the same way can allow literal
                                 transcription of existing responsibility statements and simplify programmatic
                                 processing. The following example demonstrates how a responsibility statement may
                                 be
                                 transcribed using interleaved <a class="link_odd_elementSpec" href="/documentation/2.1.1/resp">resp</a> and <a class="link_odd_elementSpec" href="/documentation/2.1.1/persName">persName</a> elements:
                              </p>
                              <div id="index.xml-egXML-d39e2471" class="pre egXML_valid">
                                 <span data-indentation="1" class="element">&lt;titleStmt&gt;</span><br />   <span data-indentation="2" class="element">&lt;title&gt;</span>Symphony No. 5 in C Minor : an electronic transcription<span data-indentation="2" class="element">&lt;/title&gt;</span><br />   <span data-indentation="2" class="element">&lt;respStmt&gt;</span><br />     <span data-indentation="3" class="element">&lt;resp&gt;</span>Composed by: <span data-indentation="3" class="element">&lt;/resp&gt;</span><br />
                                     <span data-indentation="3" class="element">&lt;persName <span class="attribute">role</span>="<span class="attributevalue">composer</span>"&gt;</span>Ludwig van Beethoven<span data-indentation="3" class="element">&lt;/persName&gt;</span><br />     <span data-indentation="3" class="element">&lt;persName <span class="attribute">role</span>="<span class="attributevalue">encoder</span>"&gt;</span>Johannes Jones:<span data-indentation="3" class="element">&lt;/persName&gt;</span><br />     <span data-indentation="3" class="element">&lt;resp&gt;</span>Machine-readable transcription<span data-indentation="3" class="element">&lt;/resp&gt;</span><br />   <span data-indentation="2" class="element">&lt;/respStmt&gt;</span><br />
                                 <span data-indentation="1" class="element">&lt;/titleStmt&gt;</span>
                                 
                              </div>
                              <p>However, eliminating explanatory text and relying on standardized values for
                                 <span class="att">role</span>, as in the following example, allows data creation and
                                 processing tools of the greatest simplicity.
                              </p>
                              <div id="index.xml-egXML-d39e2499" class="pre egXML_valid">
                                 <span data-indentation="1" class="element">&lt;titleStmt&gt;</span><br />   <span data-indentation="2" class="element">&lt;title&gt;</span>Symphony No. 5 in C Minor : an electronic transcription<span data-indentation="2" class="element">&lt;/title&gt;</span><br />   <span data-indentation="2" class="element">&lt;respStmt&gt;</span><br />     <span data-indentation="3" class="element">&lt;persName <span class="attribute">role</span>="<span class="attributevalue">composer</span>"&gt;</span>Ludwig van Beethoven<span data-indentation="3" class="element">&lt;/persName&gt;</span><br />     <span data-indentation="3" class="element">&lt;persName <span class="attribute">role</span>="<span class="attributevalue">editor</span>"&gt;</span>Johannes Jones<span data-indentation="3" class="element">&lt;/persName&gt;</span><br />   <span data-indentation="2" class="element">&lt;/respStmt&gt;</span><br />
                                 <span data-indentation="1" class="element">&lt;/titleStmt&gt;</span>
                                 
                              </div>
                           </div>
                           <div class="div3" id="editionstmt">
                              <h3><span class="headingNumber">2.1.2
                                    </span><span class="head">Edition Statement</span></h3>
                              <p>The <a class="link_odd_elementSpec" href="/documentation/2.1.1/editionStmt">editionStmt</a> element is the second component of the <a class="link_odd_elementSpec" href="/documentation/2.1.1/fileDesc">fileDesc</a> element. It is optional but recommended when
                                 applicable.
                              </p>
                              <ul class="specList">
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/editionStmt">editionStmt</a></span>
                                    (edition statement) – Container for meta-data pertaining to a particular edition of
                                    the material being described.
                                 </li>
                                 
                              </ul>
                              <p>It contains elements for identifying the edition and those responsible for
                                 it:
                              </p>
                              <ul class="specList">
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/edition">edition</a></span> (edition
                                    designation) – A word or text phrase that indicates a difference in either content
                                    or form between the item being described and a related item previously issued by the
                                    same publisher/distributor (e.g. 2nd edition, version 2.0, etc.), or simultaneously
                                    issued by either the same publisher/distributor or another publisher/distributor
                                    (e.g. large print edition, British edition, etc.).
                                 </li>
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/respStmt">respStmt</a></span>
                                    (responsibility statement) – Names one or more individuals, groups, or in rare
                                    cases, mechanical processes, responsible for creation or realization of the
                                    intellectual or artistic content.
                                 </li>
                                 
                              </ul>
                              <p>For printed texts, the term ‘edition’ applies to the set of all the identical
                                 copies of an item produced from one master copy and issued by a particular publishing
                                 agency or a group of such agencies. A change in the identity of the distributing body
                                 or bodies does not normally constitute a change of edition, while a change in the
                                 master copy does.
                              </p>
                              <p>For electronic texts, the notion of a <span class="mentioned">master copy</span> is not entirely appropriate, since they are far more easily
                                 copied and modified than printed ones; nonetheless, the term edition may be used for
                                 a
                                 particular state of a machine-readable text at which substantive changes are made
                                 and
                                 fixed. Synonymous terms used in these Guidelines are <span class="mentioned">version</span>, <span class="mentioned">level</span>, and <span class="mentioned">release</span>. The words <span class="mentioned">revision</span> and <span class="mentioned">update</span>, by contrast, are used for minor changes to a file
                                 which do not amount to a new edition.
                              </p>
                              <p>No simple rule can specify how substantive
                                 changes have to be before they are regarded as producing a new edition, rather than
                                 a
                                 simple update. The general principle proposed here is that the production of a new
                                 edition entails a significant change in the intellectual content of the file, rather
                                 than its encoding or appearance. The addition of analytic coding to a text would thus
                                 constitute a new edition, while automatic conversion from one coded representation
                                 to
                                 another would not. Changes relating to the character code or physical storage details,
                                 corrections of misspellings, simple changes in the arrangement of the contents and
                                 changes in the output format do not normally constitute a new edition, whereas the
                                 addition of new information (e.g., annotations, sound or images, links to external
                                 data) almost always does.
                              </p>
                              <p>Clearly, there will always be borderline cases and the
                                 matter is somewhat arbitrary. The simplest rule is: if you think that your file is
                                 a
                                 new edition, then call it such. An edition statement is optional for the first release
                                 of a computer file; it is mandatory for each later release, though this requirement
                                 cannot be enforced.
                              </p>
                              <p>Note that all changes in a file, whether or not they are
                                 regarded as constituting a new edition or simply a revision, should be independently
                                 noted in the revision description section of the file header (see section <a class="link_ptr" href="/documentation/2.1.1/header#revisionDescription" title="Revision Description"><span class="headingNumber">2.4 </span>Revision Description</a>).
                              </p>
                              <p>The edition
                                 element should contain phrases describing the edition or version, including the word
                                 'edition', 'version', or an equivalent term, together with a number or date, or terms
                                 indicating difference from other editions such as 'new edition', 'revised edition',
                                 etc. Any dates that occur within the edition statement should be marked with the <a class="link_odd_elementSpec" href="/documentation/2.1.1/date">date</a> element. The <span class="att">n</span> attribute of
                                 the edition element may be used as elsewhere to supply any formal identification (such
                                 as a version number) for the edition.
                              </p>
                              <p>One or more <a class="link_odd_elementSpec" href="/documentation/2.1.1/respStmt">respStmt</a> elements may also be used to supply statements of
                                 responsibility for the edition in question. These may refer to individuals or
                                 corporate bodies and can indicate functions such as that of a reviser, or can name
                                 the
                                 person or body responsible for the provision of supplementary matter, of appendices,
                                 etc., in a new edition.
                              </p>
                              <p>Some examples follow:</p>
                              <div id="index.xml-egXML-d39e2590" class="pre egXML_valid">
                                 <span data-indentation="1" class="element">&lt;editionStmt&gt;</span><br />   <span data-indentation="2" class="element">&lt;edition <span class="attribute">n</span>="<span class="attributevalue">Draft2</span>"&gt;</span>Second draft, substantially extended, revised, and
                                     corrected.<span data-indentation="2" class="element">&lt;/edition&gt;</span><br />
                                 <span data-indentation="1" class="element">&lt;/editionStmt&gt;</span>
                                 
                              </div>
                              <div id="index.xml-egXML-d39e2598" class="pre egXML_valid">
                                 <span data-indentation="1" class="element">&lt;editionStmt&gt;</span><br />   <span data-indentation="2" class="element">&lt;edition&gt;</span><br />Student's edition, <span data-indentation="3" class="element">&lt;date&gt;</span>June 1987<span data-indentation="3" class="element">&lt;/date&gt;</span><br /><span data-indentation="2" class="element">&lt;/edition&gt;</span><br />   <span data-indentation="2" class="element">&lt;respStmt&gt;</span><br />     <span data-indentation="3" class="element">&lt;resp&gt;</span>New annotations by<span data-indentation="3" class="element">&lt;/resp&gt;</span><br />
                                     <span data-indentation="3" class="element">&lt;name&gt;</span>George Brown<span data-indentation="3" class="element">&lt;/name&gt;</span><br />   <span data-indentation="2" class="element">&lt;/respStmt&gt;</span><br />
                                 <span data-indentation="1" class="element">&lt;/editionStmt&gt;</span>
                                 
                              </div>
                           </div>
                           <div class="div3" id="physicalDescription">
                              <h3><span class="headingNumber">2.1.3 </span><span class="head">Physical Description of the File</span></h3>
                              <p>The
                                 third component of the fileDesc is a description of the physical qualities of the
                                 file. The <a class="link_odd_elementSpec" href="/documentation/2.1.1/extent">extent</a> element is provided for this
                                 purpose.
                              </p>
                              <ul class="specList">
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/extent">extent</a></span> Used to
                                    express size in terms other than physical dimensions, such as number of pages,
                                    number of records in file, number of bytes, performance duration for music, audio
                                    recordings and visual projections, etc.
                                 </li>
                                 
                              </ul>
                              <p>The <a class="link_odd_elementSpec" href="/documentation/2.1.1/extent">extent</a> element describes the approximate
                                 size of a text as stored on some carrier medium, whether digital or non-digital,
                                 specified in any convenient units.
                              </p>
                              <p>For printed books, information about the
                                 carrier, such as the kind of medium used and its size, are of great importance in
                                 cataloging procedures. The print-oriented rules for bibliographic description of an
                                 item's medium and extent need some re-interpretation when applied to electronic media.
                                 An electronic file exists as a distinct entity quite independently of its carrier
                                 and
                                 remains the same intellectual object whether it is stored as file on a hard disc
                                 drive, a CD-ROM, a set of USB devices, or in the internet. Since, moreover, these
                                 Guidelines are specifically aimed at facilitating transparent document storage and
                                 interchange, any purely machine-dependent information should be irrelevant as far
                                 as
                                 the file header is concerned.
                              </p>
                              <p>This is particularly true of information about
                                 file-type although library-oriented rules for cataloging often distinguish two types
                                 of computer file: ‘data’ and ‘programs’. This distinction is quite difficult to draw
                                 in some cases, for example, hypermedia or texts with built-in search and retrieval
                                 software.
                              </p>
                              <p>Although it is equally system-dependent, some measure of the size of
                                 the computer file may be of use for cataloging and other practical purposes. Because
                                 the measurement and expression of file size is fraught with difficulties, only very
                                 general recommendations are possible; the element <a class="link_odd_elementSpec" href="/documentation/2.1.1/extent">extent</a> should contain a phrase indicating the size or approximate
                                 size of the computer file in one of the following ways:
                              </p>
                              <ul>
                                 
                                 <li class="item">in bytes of a specified length (e.g. ‘4000 bytes’)</li>
                                 
                                 <li class="item">as falling within a range of values, for example: 
                                    <ul>
                                       
                                       <li class="item">less than 1 Mb</li>
                                       
                                       <li class="item">between 1 Mb and 5 Mb</li>
                                       
                                       <li class="item">between 6 Mb and 10 Mb</li>
                                       
                                       <li class="item">over 10 Mb</li>
                                       
                                    </ul>
                                 </li>
                                 
                                 <li class="item">in terms of any convenient logical units (for example, words or
                                    sentences, citations, paragraphs)
                                 </li>
                                 
                                 <li class="item">in terms of any convenient physical units (for example, compact
                                    discs, removable hard drives, DVDs)
                                 </li>
                                 
                              </ul>
                              <p>The use of standard abbreviations for units of quantity is recommended where
                                 applicable, here as elsewhere (see <a class="link_ref" href="http://physics.nist.gov/cuu/Units/binary.html">http://physics.nist.gov/cuu/Units/binary.html</a>).
                              </p>
                              <div id="index.xml-egXML-d39e2668" class="pre egXML_invalid">
                                 <span data-indentation="1" class="element">&lt;extent&gt;</span>between 1 MB and 2 MB<span data-indentation="1" class="element">&lt;/extent&gt;</span><br />
                                 <span data-indentation="1" class="element">&lt;extent&gt;</span>4.2 MiB<span data-indentation="1" class="element">&lt;/extent&gt;</span><br />
                                 <span data-indentation="1" class="element">&lt;extent&gt;</span>4532 Mbytes<span data-indentation="1" class="element">&lt;/extent&gt;</span><br />
                                 <span data-indentation="1" class="element">&lt;extent&gt;</span>3200 sentences<span data-indentation="1" class="element">&lt;/extent&gt;</span><br />
                                 <span data-indentation="1" class="element">&lt;extent&gt;</span>5 90-mm high density diskettes<span data-indentation="1" class="element">&lt;/extent&gt;</span>
                                 
                              </div>
                              <p>For ease of processability, the use of the <span class="att">unit</span>
                                 attribute is recommended, as in the following example:
                              </p>
                              <div id="index.xml-egXML-d39e2691" class="pre egXML_valid">
                                 <span data-indentation="1" class="element">&lt;extent <span class="attribute">unit</span>="<span class="attributevalue">sentence</span>"&gt;</span>3200<span data-indentation="1" class="element">&lt;/extent&gt;</span>
                                 
                              </div>
                           </div>
                           <div class="div3" id="publicationDistribution">
                              <h3><span class="headingNumber">2.1.4 </span><span class="head">Publication, Distribution,
                                    etc.</span></h3>
                              <p>The <a class="link_odd_elementSpec" href="/documentation/2.1.1/pubStmt">pubStmt</a> element is the fourth
                                 component of the <a class="link_odd_elementSpec" href="/documentation/2.1.1/fileDesc">fileDesc</a> element and is
                                 mandatory.
                              </p>
                              <ul class="specList">
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/pubStmt">pubStmt</a></span>
                                    (publication statement) – Container for information regarding the publication or
                                    distribution of a bibliographic item, including the publisher's name and address,
                                    the date of publication, and other relevant details.
                                 </li>
                                 
                              </ul>
                              <p>It may contain either a single <a class="link_odd_elementSpec" href="/documentation/2.1.1/unpub">unpub</a> element,
                                 indicating that the file has yet to be published, or in the case of published
                                 material, one or more elements from the <a class="link_odd" href="/documentation/2.1.1/model.pubStmtPart">model.pubStmtPart</a> class. The following elements may be used to provide details
                                 regarding the file's publication and distribution:
                              </p>
                              <ul class="specList">
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/address">address</a></span> Contains
                                    a postal address, for example of a publisher, an organization, or an
                                    individual.
                                 </li>
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/availability">availability</a></span>
                                    Groups elements that describe the availability of and access to a bibliographic
                                    item, including an MEI-encoded document.
                                 </li>
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/date">date</a></span> A string
                                    identifying a point in time or the time period between two such points.
                                 </li>
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/distributor">distributor</a></span>
                                    Name of a person or other agency responsible for the distribution of a bibliographic
                                    item.
                                 </li>
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/identifier">identifier</a></span> An
                                    alpha-numeric string that establishes the identity of the described material.
                                 </li>
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/publisher">publisher</a></span> Name
                                    of the organization responsible for the publication of a bibliographic item.
                                 </li>
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/pubPlace">pubPlace</a></span>
                                    (publication place) – Name of the place where a bibliographic item was
                                    published.
                                 </li>
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/respStmt">respStmt</a></span>
                                    (responsibility statement) – Names one or more individuals, groups, or in rare
                                    cases, mechanical processes, responsible for creation or realization of the
                                    intellectual or artistic content.
                                 </li>
                                 
                              </ul>
                              <p>The publisher is the person or institution by whose authority a given edition of
                                 the file is made public. The distributor is the person or institution from whom copies
                                 of the text may be obtained. Use <a class="link_odd_elementSpec" href="/documentation/2.1.1/respStmt">respStmt</a> to identify
                                 other responsible persons or corporate bodies.
                              </p>
                              <p>The sub-elements of <a class="link_odd_elementSpec" href="/documentation/2.1.1/availability">availability</a> should be used to provide detailed
                                 information regarding access to the MEI file.
                              </p>
                              <ul class="specList">
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/acqSource">acqSource</a></span>
                                    (acquisition source) – Post-publication source, such as a vendor or distributor,
                                    from which access to a bibliographic item may be obtained, including electronic
                                    access.
                                 </li>
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/accessRestrict">accessRestrict</a></span> (access restriction) – Describes the conditions that
                                    affect the accessibility of material.
                                 </li>
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/price">price</a></span> The cost of
                                    access to a bibliographic item.
                                 </li>
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/useRestrict">useRestrict</a></span>
                                    (usage restrictions) – Container for information about the conditions that affect
                                    use of a bibliographic item after access has been granted.
                                 </li>
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/sysReq">sysReq</a></span> (system
                                    requirements) – System requirements for using the electronic item.
                                 </li>
                                 
                              </ul>
                              <div id="index.xml-egXML-d39e2752" class="pre egXML_valid">
                                 <span data-indentation="1" class="element">&lt;pubStmt
                                    xmlns="http://www.music-encoding.org/ns/mei"&gt;</span><br />   <span data-indentation="2" class="element">&lt;publisher&gt;</span><br />     <span data-indentation="3" class="element">&lt;corpName&gt;</span>Musikwissenschaftliches Seminar &lt;Detmold&gt;<span data-indentation="3" class="element">&lt;/corpName&gt;</span><br />   <span data-indentation="2" class="element">&lt;/publisher&gt;</span><br />   <span data-indentation="2" class="element">&lt;address&gt;</span><br />     <span data-indentation="3" class="element">&lt;addrLine&gt;</span>Gartenstrasse 20<span data-indentation="3" class="element">&lt;/addrLine&gt;</span><br />     <span data-indentation="3" class="element">&lt;addrLine&gt;</span><br />32756 <span data-indentation="4" class="element">&lt;geogName&gt;</span>Detmold<span data-indentation="4" class="element">&lt;/geogName&gt;</span><br /><span data-indentation="3" class="element">&lt;/addrLine&gt;</span><br />     <span data-indentation="3" class="element">&lt;addrLine&gt;</span><br /><span data-indentation="4" class="element">&lt;geogName&gt;</span>Germany<span data-indentation="4" class="element">&lt;/geogName&gt;</span><br /><span data-indentation="3" class="element">&lt;/addrLine&gt;</span><br />   <span data-indentation="2" class="element">&lt;/address&gt;</span><br />   <span data-indentation="2" class="element">&lt;date&gt;</span>2011<span data-indentation="2" class="element">&lt;/date&gt;</span><br />
                                   <span data-indentation="2" class="element">&lt;availability&gt;</span><br />     <span data-indentation="3" class="element">&lt;useRestrict&gt;</span>© 2004, MEI Consortium<span data-indentation="3" class="element">&lt;/useRestrict&gt;</span><br />   <span data-indentation="2" class="element">&lt;/availability&gt;</span><br />
                                 <span data-indentation="1" class="element">&lt;/pubStmt&gt;</span>
                                 
                              </div>
                              <div id="index.xml-egXML-d39e2787" class="pre egXML_valid">
                                 <span data-indentation="1" class="element">&lt;pubStmt
                                    xmlns="http://www.music-encoding.org/ns/mei"&gt;</span><br />   <span data-indentation="2" class="element">&lt;publisher&gt;</span><br />     <span data-indentation="3" class="element">&lt;corpName&gt;</span>Segno Press Inc.<span data-indentation="3" class="element">&lt;/corpName&gt;</span><br />   <span data-indentation="2" class="element">&lt;/publisher&gt;</span><br />   <span data-indentation="2" class="element">&lt;distributor&gt;</span><br />     <span data-indentation="3" class="element">&lt;corpName&gt;</span>University of Virginia<span data-indentation="3" class="element">&lt;/corpName&gt;</span><br />     <span data-indentation="3" class="element">&lt;address&gt;</span><br />
                                       <span data-indentation="4" class="element">&lt;addrLine&gt;</span>221 B LowWater Street,<span data-indentation="4" class="element">&lt;/addrLine&gt;</span><br />       <span data-indentation="4" class="element">&lt;addrLine&gt;</span>Charlottesville, Virginia<span data-indentation="4" class="element">&lt;/addrLine&gt;</span><br />       <span data-indentation="4" class="element">&lt;addrLine&gt;</span>22901<span data-indentation="4" class="element">&lt;/addrLine&gt;</span><br />   <span data-indentation="3" class="element">&lt;/address&gt;</span><br />   <span data-indentation="2" class="element">&lt;/distributor&gt;</span><br />   <span data-indentation="2" class="element">&lt;date&gt;</span>2010<span data-indentation="2" class="element">&lt;/date&gt;</span><br />   <span data-indentation="2" class="element">&lt;identifier&gt;</span>1234<span data-indentation="2" class="element">&lt;/identifier&gt;</span><br />
                                   <span data-indentation="2" class="element">&lt;availability&gt;</span><br />     <span data-indentation="3" class="element">&lt;useRestrict&gt;</span>Available for purposes of academic research and teaching
                                       only.<span data-indentation="3" class="element">&lt;/useRestrict&gt;</span><br />   <span data-indentation="2" class="element">&lt;/availability&gt;</span><br />
                                 <span data-indentation="1" class="element">&lt;/pubStmt&gt;</span>
                                 
                              </div>
                              <p>Give any other useful information (e.g., dates of collection of data) in an
                                 annotation within the notes statement, which is described below.
                              </p>
                              <p>Here, as in the
                                 description of intellectual responsibility described above, the <a class="link_odd_elementSpec" href="/documentation/2.1.1/respStmt">respStmt</a> element may be used to contain all statements of
                                 responsibility regarding publication and distribution when uniformity is desired
                                 regardless of the role of participants in the publication process:
                              </p>
                              <div id="index.xml-egXML-d39e2836" class="pre egXML_valid">
                                 <span data-indentation="1" class="element">&lt;respStmt
                                    xmlns="http://www.music-encoding.org/ns/mei"&gt;</span><br />   <span data-indentation="2" class="element">&lt;corpName <span class="attribute">role</span>="<span class="attributevalue">publisher</span>"&gt;</span>MEI Project<span data-indentation="2" class="element">&lt;/corpName&gt;</span><br />   <span data-indentation="2" class="element">&lt;corpName <span class="attribute">authURI</span>="<span class="attributevalue">http://d-nb.info/gnd</span>" <span class="attribute">authority</span>="<span class="attributevalue">GND</span>" <span class="attribute">dbkey</span>="<span class="attributevalue">2007744-0</span>" <span class="attribute">role</span>="<span class="attributevalue">funder</span>"&gt;</span>German Research Foundation<span data-indentation="2" class="element">&lt;/corpName&gt;</span><br />   <span data-indentation="2" class="element">&lt;corpName <span class="attribute">authURI</span>="<span class="attributevalue">http://d-nb.info/gnd/18183-3</span>" <span class="attribute">authority</span>="<span class="attributevalue">Deutsche
                                       Nationalbibliothek</span>" <span class="attribute">dbkey</span>="<span class="attributevalue">18183-3</span>" <span class="attribute">role</span>="<span class="attributevalue">funder</span>"&gt;</span> National Endowment for the
                                     Humanities<span data-indentation="2" class="element">&lt;/corpName&gt;</span><br />
                                 <span data-indentation="1" class="element">&lt;/respStmt&gt;</span>
                                 
                              </div>
                           </div>
                           <div class="div3" id="seriesStatement">
                              <h3><span class="headingNumber">2.1.5
                                    </span><span class="head">Series Statement</span></h3>
                              <p>The <a class="link_odd_elementSpec" href="/documentation/2.1.1/seriesStmt">seriesStmt</a> element is the fifth component of the <a class="link_odd_elementSpec" href="/documentation/2.1.1/fileDesc">fileDesc</a> element and is optional.
                              </p>
                              <ul class="specList">
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/seriesStmt">seriesStmt</a></span>
                                    (series statement) – Groups information about the series, if any, to which a
                                    publication belongs.
                                 </li>
                                 
                              </ul>
                              <p>A series may be defined in one of the following ways:</p>
                              <ul>
                                 
                                 <li class="item">A group of separate items related to one another by the fact that
                                    each item bears, in addition to its own title proper, a collective title applying
                                    to
                                    the group as a whole. The individual items may or may not be numbered.
                                 </li>
                                 
                                 <li class="item">Each of two or more volumes of essays, lectures, articles, or other
                                    items, similar in character and issued in sequence.
                                 </li>
                                 
                                 <li class="item">A separately numbered sequence of volumes within a series or
                                    serial.
                                 </li>
                                 
                              </ul>
                              <p>The <a class="link_odd_elementSpec" href="/documentation/2.1.1/seriesStmt">seriesStmt</a> element may contain one or more
                                 of the following more specific elements:
                              </p>
                              <ul class="specList">
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/title">title</a></span> Title of a
                                    bibliographic entity.
                                 </li>
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/editor">editor</a></span> The name of
                                    the individual(s), institution(s) or organization(s) acting in an editorial
                                    capacity.
                                 </li>
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/respStmt">respStmt</a></span>
                                    (responsibility statement) – Names one or more individuals, groups, or in rare
                                    cases, mechanical processes, responsible for creation or realization of the
                                    intellectual or artistic content.
                                 </li>
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/identifier">identifier</a></span> An
                                    alpha-numeric string that establishes the identity of the described material.
                                 </li>
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/contents">contents</a></span>
                                    Description of the material contained within a resource.
                                 </li>
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/seriesStmt">seriesStmt</a></span>
                                    (series statement) – Groups information about the series, if any, to which a
                                    publication belongs.
                                 </li>
                                 
                              </ul>
                              <p>The <a class="link_odd_elementSpec" href="/documentation/2.1.1/title">title</a>, <a class="link_odd_elementSpec" href="/documentation/2.1.1/editor">editor</a> and <a class="link_odd_elementSpec" href="/documentation/2.1.1/identifier">identifier</a> elements have
                                 the same function described above: identification of the item, in this case the
                                 series, and the individuals or groups responsible for its creation. The <a class="link_odd_elementSpec" href="/documentation/2.1.1/title">title</a> element is required within <a class="link_odd_elementSpec" href="/documentation/2.1.1/seriesStmt">seriesStmt</a>.
                              </p>
                              <div id="index.xml-egXML-d39e2907" class="pre egXML_valid">
                                 <span data-indentation="1" class="element">&lt;seriesStmt&gt;</span><br />   <span data-indentation="2" class="element">&lt;title&gt;</span>MEI Sample Collection<span data-indentation="2" class="element">&lt;/title&gt;</span><br />
                                 <span data-indentation="1" class="element">&lt;/seriesStmt&gt;</span>
                                 
                              </div>
                              <p>The <a class="link_odd_elementSpec" href="/documentation/2.1.1/identifier">identifier</a> element may be used to supply
                                 any identifying number associated with the series, including both standard numbers
                                 such as an ISSN and particular issue numbers. Its <span class="att">type</span>
                                 attribute is used to categorize the number further, taking the value 'ISSN' for an
                                 ISSN, for example.
                              </p>
                              <div id="index.xml-egXML-d39e2923" class="pre egXML_valid">
                                 <span data-indentation="1" class="element">&lt;seriesStmt&gt;</span><br />   <span data-indentation="2" class="element">&lt;title <span class="attribute">level</span>="<span class="attributevalue">s</span>"&gt;</span>Studies in Ornamentation<span data-indentation="2" class="element">&lt;/title&gt;</span><br />   <span data-indentation="2" class="element">&lt;editor&gt;</span>Jacques Composeur<span data-indentation="2" class="element">&lt;/editor&gt;</span><br />
                                   <span data-indentation="2" class="element">&lt;identifier <span class="attribute">type</span>="<span class="attributevalue">ISSN</span>"&gt;</span>0-345-6789<span data-indentation="2" class="element">&lt;/identifier&gt;</span><br />
                                 <span data-indentation="1" class="element">&lt;/seriesStmt&gt;</span>
                                 
                              </div>
                              <p>The contents of the series may be enumerated using the <a class="link_odd_elementSpec" href="/documentation/2.1.1/contents">contents</a> element. Use of this element should be determined by the
                                 complexity of the resource and whether or not the information is readily available.
                                 The <a class="link_odd_elementSpec" href="/documentation/2.1.1/contents">contents</a> element may consist of a single paragraph
                                 when unstructured information is sufficient.
                              </p>
                              <div id="index.xml-egXML-d39e2946" class="pre egXML_valid">
                                 <span data-indentation="1" class="element">&lt;contents&gt;</span><br />   <span data-indentation="2" class="element">&lt;p&gt;</span>On Wenlock Edge -- From Far, From Eve and Morning -- Is My Team Ploughing? -- Oh, When
                                     I Was In Love With You -- Bredon Hill -- Clun<span data-indentation="2" class="element">&lt;/p&gt;</span><br />
                                 <span data-indentation="1" class="element">&lt;/contents&gt;</span>
                                 
                              </div>
                              <p>Alternatively, <a class="link_odd_elementSpec" href="/documentation/2.1.1/contentItem">contentItem</a> elements may be used
                                 to provide structure for the content description.
                              </p>
                              <div id="index.xml-egXML-d39e2959" class="pre egXML_valid">
                                 <span data-indentation="1" class="element">&lt;contents&gt;</span><br />   <span data-indentation="2" class="element">&lt;head&gt;</span>Contents<span data-indentation="2" class="element">&lt;/head&gt;</span><br />   <span data-indentation="2" class="element">&lt;contentItem&gt;</span>On Wenlock Edge<span data-indentation="2" class="element">&lt;/contentItem&gt;</span><br />   <span data-indentation="2" class="element">&lt;contentItem&gt;</span>From Far, From Eve and Morning<span data-indentation="2" class="element">&lt;/contentItem&gt;</span><br />   <span data-indentation="2" class="element">&lt;contentItem&gt;</span>Is My Team Ploughing?<span data-indentation="2" class="element">&lt;/contentItem&gt;</span><br />   <span data-indentation="2" class="element">&lt;contentItem&gt;</span>Oh, When I Was In Love With You<span data-indentation="2" class="element">&lt;/contentItem&gt;</span><br />   <span data-indentation="2" class="element">&lt;contentItem&gt;</span>Bredon Hill<span data-indentation="2" class="element">&lt;/contentItem&gt;</span><br />   <span data-indentation="2" class="element">&lt;contentItem&gt;</span>Clun<span data-indentation="2" class="element">&lt;/contentItem&gt;</span><br />
                                 <span data-indentation="1" class="element">&lt;/contents&gt;</span>
                                 
                              </div>
                              <p>Finally, using the <span class="att">target</span> attribute, a link to an
                                 external table of contents may be supplied in lieu of or in addition to the child
                                 elements of <a class="link_odd_elementSpec" href="/documentation/2.1.1/contents">contents</a>.
                              </p>
                              <div id="index.xml-egXML-d39e2994" class="pre egXML_valid">
                                 <span data-indentation="1" class="element">&lt;contents <span class="attribute">target</span>="<span class="attributevalue">http://www.series.content/12345</span>"/&gt;</span>
                                 
                              </div>
                              <p>The <a class="link_odd_elementSpec" href="/documentation/2.1.1/seriesStmt">seriesStmt</a> element is allowed to nest
                                 within itself in order to accommodate a series within a series.
                              </p>
                           </div>
                           <div class="div3" id="notesStatement">
                              <h3><span class="headingNumber">2.1.6 </span><span class="head">Notes Statement</span></h3>
                              <p>The <a class="link_odd_elementSpec" href="/documentation/2.1.1/notesStmt">notesStmt</a> element is the sixth component of the <a class="link_odd_elementSpec" href="/documentation/2.1.1/fileDesc">fileDesc</a> element and is optional. If used, it contains one or more
                                 <a class="link_odd_elementSpec" href="/documentation/2.1.1/annot">annot</a> elements, each containing a single piece of
                                 descriptive information of the kind treated as ‘general notes’ in traditional
                                 bibliographic descriptions.
                              </p>
                              <ul class="specList">
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/notesStmt">notesStmt</a></span>
                                    (notes statement)– Collects any notes providing information about a text additional
                                    to that recorded in other parts of the bibliographic description.
                                 </li>
                                 
                              </ul>
                              <p>Some information found in the notes area in conventional bibliography has been
                                 assigned specific elements in these Guidelines; in particular the following items
                                 should be tagged as indicated, rather than as general notes:
                              </p>
                              <ul>
                                 
                                 <li class="item">the nature, scope, artistic form, or purpose of the work; also the
                                    genre or other intellectual category to which it may belong. These should be
                                    formally described within the <a class="link_odd_elementSpec" href="/documentation/2.1.1/workDesc">workDesc</a> element
                                    (section <a class="link_ptr" href="/documentation/2.1.1/header#workDescription" title="Work Description"><span class="headingNumber">2.3 </span>Work Description</a>).
                                 </li>
                                 
                                 <li class="item">bibliographic details relating to the source or sources of an
                                    electronic text: e.g., ‘Transcribed from a facsimile of the 1743 publication’. These
                                    should be formally described in the <a class="link_odd_elementSpec" href="/documentation/2.1.1/sourceDesc">sourceDesc</a>
                                    element (section <a class="link_ptr" href="/documentation/2.1.1/header#sourceDescription" title="Source Description"><span class="headingNumber">2.1.7 </span>Source
                                       Description</a>).
                                 </li>
                                 
                                 <li class="item">further information relating to publication, distribution, or release
                                    of the text, including sources from which the text may be obtained, any restrictions
                                    on its use or formal terms on its availability. These should be placed in the
                                    appropriate division of the <a class="link_odd_elementSpec" href="/documentation/2.1.1/pubStmt">pubStmt</a> element (section
                                    <a class="link_ptr" href="/documentation/2.1.1/header#publicationDistribution" title="Publication Distribution etc."><span class="headingNumber">2.1.4
                                          </span>Publication, Distribution, etc.</a>).
                                 </li>
                                 
                                 <li class="item">publicly documented numbers associated <em>with the file</em> should
                                    be placed in an <a class="link_odd_elementSpec" href="/documentation/2.1.1/altId">altId</a> element within the <a class="link_odd_elementSpec" href="/documentation/2.1.1/meiHead">meiHead</a> element. International Standard Serial Numbers
                                    (ISSN), International Standard Book Numbers (ISBN), and other internationally agreed
                                    upon standard numbers that uniquely identify an item, should be treated in the same
                                    way, rather than as specialized bibliographic notes. As described elsewhere,
                                    identifiers <em>for sources of the file</em> should be recorded within the <a class="link_odd_elementSpec" href="/documentation/2.1.1/sourceDesc">sourceDesc</a>.
                                 </li>
                                 
                              </ul>
                              <p>Nevertheless, the <a class="link_odd_elementSpec" href="/documentation/2.1.1/notesStmt">notesStmt</a> element may be used
                                 to record potentially significant details about the file and its features, for
                                 example:
                              </p>
                              <ul>
                                 
                                 <li class="item">dates, when they are relevant to the content or condition of the
                                    computer file: e.g. ‘manual dated 2010’, ‘file validated Apr 2011’
                                 </li>
                                 
                                 <li class="item">names of persons or bodies connected with the technical production,
                                    administration, or consulting functions of the effort which produced the file, if
                                    these are not named in statements of responsibility in the title or edition
                                    statements of the file description: e.g. ‘Historical commentary provided by members
                                    of the Big Symphony Orchestra’
                                 </li>
                                 
                                 <li class="item">availability of the file in an additional medium or information not
                                    already recorded about the availability of documentation: e.g. ‘User manual is
                                    loose-leaf in eleven paginated sections’
                                 </li>
                                 
                                 <li class="item">language of work and abstract, if not encoded in the <a class="link_odd_elementSpec" href="/documentation/2.1.1/langUsage">langUsage</a> element, e.g. ‘Text in English with stage directions in
                                    French and German’
                                 </li>
                                 
                              </ul>
                              <p>Each such item of information may be tagged using the general-purpose <a class="link_odd_elementSpec" href="/documentation/2.1.1/annot">annot</a> element. Groups of annotations are contained within
                                 the <a class="link_odd_elementSpec" href="/documentation/2.1.1/notesStmt">notesStmt</a> element, as in the following
                                 example:
                              </p>
                              <div id="index.xml-egXML-d39e3088" class="pre egXML_valid">
                                 <span data-indentation="1" class="element">&lt;notesStmt&gt;</span><br />   <span data-indentation="2" class="element">&lt;annot&gt;</span>Historical commentary provided by John Smith.<span data-indentation="2" class="element">&lt;/annot&gt;</span><br />   <span data-indentation="2" class="element">&lt;annot&gt;</span>OCR scanning performed at University of Virginia.<span data-indentation="2" class="element">&lt;/annot&gt;</span><br />
                                 <span data-indentation="1" class="element">&lt;/notesStmt&gt;</span>
                                 
                              </div>
                              <p>There are advantages, however, to encoding such information with more precise
                                 elements elsewhere in the MEI header, when such elements are available. For example,
                                 the notes above might be encoded as follows:
                              </p>
                              <div id="index.xml-egXML-d39e3101" class="pre egXML_valid">
                                 <span data-indentation="1" class="element">&lt;titleStmt&gt;</span><br />   <span data-indentation="2" class="element">&lt;title&gt;</span><br />…<span data-indentation="2" class="element">&lt;/title&gt;</span><br />   <span data-indentation="2" class="element">&lt;respStmt&gt;</span><br />     <span data-indentation="3" class="element">&lt;persName&gt;</span>John Smith<span data-indentation="3" class="element">&lt;/persName&gt;</span><br />
                                     <span data-indentation="3" class="element">&lt;resp&gt;</span>historical commentary<span data-indentation="3" class="element">&lt;/resp&gt;</span><br />   <span data-indentation="2" class="element">&lt;/respStmt&gt;</span><br />   <span data-indentation="2" class="element">&lt;respStmt&gt;</span><br />     <span data-indentation="3" class="element">&lt;corpName&gt;</span>University of Virginia<span data-indentation="3" class="element">&lt;/corpName&gt;</span><br />     <span data-indentation="3" class="element">&lt;resp&gt;</span>OCR scanning<span data-indentation="3" class="element">&lt;/resp&gt;</span><br />   <span data-indentation="2" class="element">&lt;/respStmt&gt;</span><br />
                                 <span data-indentation="1" class="element">&lt;/titleStmt&gt;</span>
                                 
                              </div>
                           </div>
                           <div class="div3" id="sourceDescription">
                              <h3><span class="headingNumber">2.1.7 </span><span class="head">Source Description</span></h3>
                              <p>The <a class="link_odd_elementSpec" href="/documentation/2.1.1/sourceDesc">sourceDesc</a> element is the seventh and final component of
                                 the <a class="link_odd_elementSpec" href="/documentation/2.1.1/fileDesc">fileDesc</a> element. In MEI, <a class="link_odd_elementSpec" href="/documentation/2.1.1/sourceDesc">sourceDesc</a> is a grouping element containing one or more <a class="link_odd_elementSpec" href="/documentation/2.1.1/source">source</a> elements, each of which records details of a source
                                 from which a computer file is derived. This might be a printed text or manuscript,
                                 another computer file, an audio or video recording, or a combination of these. An
                                 electronic file may also have no source, if what is being cataloged is an original
                                 text created in electronic form.
                              </p>
                              <ul class="specList">
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/sourceDesc">sourceDesc</a></span>
                                    (source description) – A container for the descriptions of the source(s) used in the
                                    creation of the electronic file.
                                 </li>
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/source">source</a></span> A
                                    bibliographic description of a source used in the creation of the electronic
                                    file.
                                 </li>
                                 
                              </ul>
                              <p>The content model of the <a class="link_odd_elementSpec" href="/documentation/2.1.1/source">source</a> element is
                                 similar to that of the <a class="link_odd_elementSpec" href="/documentation/2.1.1/fileDesc">fileDesc</a> and <a class="link_odd_elementSpec" href="/documentation/2.1.1/work">work</a> elements. The list below reflects the order in which the
                                 optional components of <a class="link_odd_elementSpec" href="/documentation/2.1.1/source">source</a> must occur.
                              </p>
                              <ul class="specList">
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/identifier">identifier</a></span> An
                                    alpha-numeric string that establishes the identity of the described material.
                                 </li>
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/titleStmt">titleStmt</a></span>
                                    (title statement) – Container for title and responsibility meta-data.
                                 </li>
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/editionStmt">editionStmt</a></span>
                                    (edition statement) – Container for meta-data pertaining to a particular edition of
                                    the material being described.
                                 </li>
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/pubStmt">pubStmt</a></span>
                                    (publication statement) – Container for information regarding the publication or
                                    distribution of a bibliographic item, including the publisher's name and address,
                                    the date of publication, and other relevant details.
                                 </li>
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/physDesc">physDesc</a></span>
                                    (physical description) – Container for information about the appearance,
                                    construction, or handling of physical materials, such as their dimension, quantity,
                                    color, style, and technique of creation.
                                 </li>
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/physLoc">physLoc</a></span> (physical
                                    location) – Groups information about the physical location of a bibliographic item,
                                    such as the repository in which it is located and its shelf mark.
                                 </li>
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/seriesStmt">seriesStmt</a></span>
                                    (series statement) – Groups information about the series, if any, to which a
                                    publication belongs.
                                 </li>
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/contents">contents</a></span>
                                    Description of the material contained within a resource.
                                 </li>
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/langUsage">langUsage</a></span>
                                    (language usage) – Groups elements describing the languages, sub-languages,
                                    dialects, etc., represented within the encoded resource.
                                 </li>
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/notesStmt">notesStmt</a></span>
                                    (notes statement)– Collects any notes providing information about a text additional
                                    to that recorded in other parts of the bibliographic description.
                                 </li>
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/classification">classification</a></span> Groups information which describes the nature or topic
                                    of an entity.
                                 </li>
                                 
                              </ul>
                              <p>When the MEI.frbr module is available, the following elements may also appear
                                 after the classification element. Additional information regarding FRBR (Functional
                                 Requirements for Bibliographic Records) can be found at <a class="link_ptr" href="/documentation/2.1.1/FRBR" title="1"><span class="headingNumber">3 </span>Functional Requirements
                                    for Bibliographic Records (FRBR)</a>.
                              </p>
                              <ul class="specList">
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/itemList">itemList</a></span> Gathers
                                    bibliographic item entities.
                                 </li>
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/componentGrp">componentGrp</a></span>
                                    (component group) – The child elements of this element are treated as parts of the
                                    elements header. Although this is an implicit way of expressing FRBR's hasPart /
                                    isPartOf -relationships, it avoids this terminology in order to prevent confusion
                                    with musical terminology. All children of a component must be the same type as its
                                    parent: works within work, items in item, etc.
                                 </li>
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/relationList">relationList</a></span>
                                    Gathers bibliographic relation elements.
                                 </li>
                                 
                              </ul>
                              <p>In the simplest case, the <a class="link_odd_elementSpec" href="/documentation/2.1.1/source">source</a> element may
                                 contain nothing more than a notes statement giving a simple prose description or a
                                 brief note stating that the document has no physical source:
                              </p>
                              <div id="index.xml-egXML-d39e3195" class="pre egXML_valid">
                                 <span data-indentation="1" class="element">&lt;sourceDesc&gt;</span><br />   <span data-indentation="2" class="element">&lt;source&gt;</span><br />     <span data-indentation="3" class="element">&lt;notesStmt&gt;</span><br />
                                       <span data-indentation="4" class="element">&lt;annot&gt;</span>Based on the Porter Wagner edition.<span data-indentation="4" class="element">&lt;/annot&gt;</span><br />     <span data-indentation="3" class="element">&lt;/notesStmt&gt;</span><br />   <span data-indentation="2" class="element">&lt;/source&gt;</span><br />
                                 <span data-indentation="1" class="element">&lt;/sourceDesc&gt;</span>
                                 
                              </div>
                              <div id="index.xml-egXML-d39e3209" class="pre egXML_valid">
                                 <span data-indentation="1" class="element">&lt;sourceDesc&gt;</span><br />   <span data-indentation="2" class="element">&lt;source&gt;</span><br />     <span data-indentation="3" class="element">&lt;notesStmt&gt;</span><br />
                                       <span data-indentation="4" class="element">&lt;annot&gt;</span>Born digital.<span data-indentation="4" class="element">&lt;/annot&gt;</span><br />     <span data-indentation="3" class="element">&lt;/notesStmt&gt;</span><br />   <span data-indentation="2" class="element">&lt;/source&gt;</span><br />
                                 <span data-indentation="1" class="element">&lt;/sourceDesc&gt;</span>
                                 
                              </div>
                              <p>Alternatively, it may contain a basic bibliographic citation, also in an
                                 annotation:
                              </p>
                              <div id="index.xml-egXML-d39e3226" class="pre egXML_valid">
                                 <span data-indentation="1" class="element">&lt;sourceDesc&gt;</span><br />   <span data-indentation="2" class="element">&lt;source&gt;</span><br />     <span data-indentation="3" class="element">&lt;notesStmt&gt;</span><br />
                                       <span data-indentation="4" class="element">&lt;annot&gt;</span>Bach, Carl Philipp Emanuel. Sonata in B-flat major, Wq.62/1 (H.2)<span data-indentation="4" class="element">&lt;/annot&gt;</span><br />     <span data-indentation="3" class="element">&lt;/notesStmt&gt;</span><br />   <span data-indentation="2" class="element">&lt;/source&gt;</span><br />
                                 <span data-indentation="1" class="element">&lt;/sourceDesc&gt;</span>
                                 
                              </div>
                              <p>However, more structured bibliographic data, such as that in the example below,
                                 facilitates better machine-processing:
                              </p>
                              <div id="index.xml-egXML-d39e3242" class="pre egXML_valid">
                                 <span data-indentation="1" class="element">&lt;sourceDesc&gt;</span><br />   <span data-indentation="2" class="element">&lt;source <span class="attribute">xml:id</span>="<span class="attributevalue">header.s1</span>"&gt;</span><br />     <span data-indentation="3" class="element">&lt;identifier&gt;</span>1<span data-indentation="3" class="element">&lt;/identifier&gt;</span><br />
                                     <span data-indentation="3" class="element">&lt;titleStmt&gt;</span><br />       <span data-indentation="4" class="element">&lt;title&gt;</span><br />Sonata in B-flat major, <span data-indentation="5" class="element">&lt;identifier&gt;</span>Wq. 62/1 (H.2)<span data-indentation="5" class="element">&lt;/identifier&gt;</span><br /><span data-indentation="4" class="element">&lt;/title&gt;</span><br />       <span data-indentation="4" class="element">&lt;respStmt&gt;</span><br />         <span data-indentation="5" class="element">&lt;name&gt;</span>Bach, Carl Philipp Emanuel<span data-indentation="5" class="element">&lt;/name&gt;</span><br />       <span data-indentation="4" class="element">&lt;/respStmt&gt;</span><br />     <span data-indentation="3" class="element">&lt;/titleStmt&gt;</span><br />     <span data-indentation="3" class="element">&lt;pubStmt&gt;</span><br />       <span data-indentation="4" class="element">&lt;pubPlace&gt;</span>Paris<span data-indentation="4" class="element">&lt;/pubPlace&gt;</span><br />
                                       <span data-indentation="4" class="element">&lt;respStmt&gt;</span><br />         <span data-indentation="5" class="element">&lt;name&gt;</span>A. Farrenc<span data-indentation="5" class="element">&lt;/name&gt;</span><br />       <span data-indentation="4" class="element">&lt;/respStmt&gt;</span><br />       <span data-indentation="4" class="element">&lt;date&gt;</span>1861-72<span data-indentation="4" class="element">&lt;/date&gt;</span><br />     <span data-indentation="3" class="element">&lt;/pubStmt&gt;</span><br />     <span data-indentation="3" class="element">&lt;seriesStmt&gt;</span><br />       <span data-indentation="4" class="element">&lt;title&gt;</span>Tresor des Pianistes, Vol. 13<span data-indentation="4" class="element">&lt;/title&gt;</span><br />     <span data-indentation="3" class="element">&lt;/seriesStmt&gt;</span><br />
                                     <span data-indentation="3" class="element">&lt;notesStmt&gt;</span><br />       <span data-indentation="4" class="element">&lt;annot&gt;</span>reprinted New York: Dover Publications, n.d.<span data-indentation="4" class="element">&lt;/annot&gt;</span><br />     <span data-indentation="3" class="element">&lt;/notesStmt&gt;</span><br />   <span data-indentation="2" class="element">&lt;/source&gt;</span><br />
                                 <span data-indentation="1" class="element">&lt;/sourceDesc&gt;</span>
                                 
                              </div>
                              <p>A description of more precise capture of dates and date ranges is provided in
                                 chapter <a class="link_ptr" href="/documentation/2.1.1/namesDates" title="0"><span class="headingNumber">18 </span>Names and Dates</a>.
                              </p>
                              <p>The <a class="link_odd_elementSpec" href="/documentation/2.1.1/identifier">identifier</a> element is provided within <a class="link_odd_elementSpec" href="/documentation/2.1.1/source">source</a> in order to accommodate identifying strings which cannot be
                                 captured by the <span class="att">xml:id</span> attribute, such as numbers or strings
                                 requiring XML markup.
                              </p>
                              <p>The <a class="link_odd_elementSpec" href="/documentation/2.1.1/titleStmt">titleStmt</a>, <a class="link_odd_elementSpec" href="/documentation/2.1.1/editionStmt">editionStmt</a>, <a class="link_odd_elementSpec" href="/documentation/2.1.1/pubStmt">pubStmt</a>,
                                 <a class="link_odd_elementSpec" href="/documentation/2.1.1/seriesStmt">seriesStmt</a>, and <a class="link_odd_elementSpec" href="/documentation/2.1.1/notesStmt">notesStmt</a> elements function in exactly the same way as described in
                                 section <a class="link_ptr" href="/documentation/2.1.1/header#fileDescription" title="File Description"><span class="headingNumber">2.1 </span>File Description</a> above and <a class="link_ptr" href="/documentation/2.1.1/header#workDescription" title="Work Description"><span class="headingNumber">2.3 </span>Work Description</a> below and will not be
                                 covered again here.
                              </p>
                              <p>If a source of the file is an unpublished manuscript, it is
                                 recommended that the <a class="link_odd_elementSpec" href="/documentation/2.1.1/unpub">unpub</a> element be used as the only
                                 content of the source's <a class="link_odd_elementSpec" href="/documentation/2.1.1/pubStmt">pubStmt</a> element. Other
                                 identifying information for the manuscript may be collected in the <a class="link_odd_elementSpec" href="/documentation/2.1.1/notesStmt">notesStmt</a> element, as described in section <a class="link_ptr" href="/documentation/2.1.1/header#notesStatement" title="Notes Statement"><span class="headingNumber">2.1.6
                                       </span>Notes Statement</a>.
                              </p>
                              <div id="index.xml-egXML-d39e3344" class="pre egXML_valid">
                                 <span data-indentation="1" class="element">&lt;source&gt;</span><br />   <span data-indentation="2" class="element">&lt;titleStmt&gt;</span><br />     <span data-indentation="3" class="element">&lt;title&gt;</span>[Untitled Bach Manuscript]<span data-indentation="3" class="element">&lt;/title&gt;</span><br />     <span data-indentation="3" class="element">&lt;respStmt&gt;</span><br />       <span data-indentation="4" class="element">&lt;persName&gt;</span>Johann Sebastian Bach<span data-indentation="4" class="element">&lt;/persName&gt;</span><br />     <span data-indentation="3" class="element">&lt;/respStmt&gt;</span><br />   <span data-indentation="2" class="element">&lt;/titleStmt&gt;</span><br />   <span data-indentation="2" class="element">&lt;pubStmt&gt;</span><br />     <span data-indentation="3" class="element">&lt;unpub/&gt;</span><br />   <span data-indentation="2" class="element">&lt;/pubStmt&gt;</span><br />   <span data-indentation="2" class="element">&lt;notesStmt&gt;</span><br />     <span data-indentation="3" class="element">&lt;annot&gt;</span>Manuscript discovered in library stacks, 2012<span data-indentation="3" class="element">&lt;/annot&gt;</span><br />   <span data-indentation="2" class="element">&lt;/notesStmt&gt;</span><br />
                                 <span data-indentation="1" class="element">&lt;/source&gt;</span>
                                 
                              </div>
                              <div class="div4" id="associatingMetadataAndData">
                                 <h4><span class="headingNumber">2.1.7.1 </span><span class="head">Associating Metadata and Data</span></h4>
                                 <p>In
                                    the MEI header, the <span class="att">data</span> attribute may be used to associate
                                    metadata with related notational elements.
                                 </p>
                                 <p>Similarly, in the body of the MEI
                                    document, the <span class="att">decls</span> attribute may be used to associate
                                    parts of the encoded text with related metadata.
                                 </p>
                                 <p>The most useful associations
                                    of this type are between the bibliographic description of a source and the material
                                    taken from it.
                                 </p>
                              </div>
                           </div>
                        </div>
                        <div class="div2" id="encodingDescription">
                           <h2><span class="headingNumber">2.2 </span><span class="head">Encoding
                                 Description</span></h2>
                           <p>The <a class="link_odd_elementSpec" href="/documentation/2.1.1/encodingDesc">encodingDesc</a> element is
                              the second major subdivision of the MEI header. It specifies the methods and editorial
                              principles which governed the transcription or encoding of the source material. Though
                              not formally required, its use is highly recommended.
                           </p>
                           <ul class="specList">
                              
                              <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/encodingDesc">encodingDesc</a></span>
                                 (encoding description) – Documents the relationship between an electronic file and
                                 the
                                 source or sources from which it was derived as well as applications used in the
                                 encoding/editing process.
                              </li>
                              
                           </ul>
                           <p>The encoding description may contain elements taken from the model.encodingPart
                              class. By default, this class makes available the following elements:
                           </p>
                           <ul class="specList">
                              
                              <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/appInfo">appInfo</a></span>
                                 (application information) – Groups information about applications which have acted
                                 upon the MEI file.
                              </li>
                              
                              <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/editorialDecl">editorialDecl</a></span>
                                 (editorial declaration) – Used to provide details of editorial principles and
                                 practices applied during the encoding of musical text.
                              </li>
                              
                              <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/projectDesc">projectDesc</a></span>
                                 (project description) – Project-level meta-data describing the aim or purpose for
                                 which the electronic file was encoded, funding agencies, etc. together with any other
                                 relevant information concerning the process by which it was assembled or
                                 collected.
                              </li>
                              
                              <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/samplingDecl">samplingDecl</a></span>
                                 (sampling declaration) – Contains a prose description of the rationale and methods
                                 used in sampling texts in the creation of a corpus or collection.
                              </li>
                              
                           </ul>
                           <p>Each of these elements is further described in the appropriate section
                              below.
                           </p>
                           <div class="div3" id="applicationInformation">
                              <h3><span class="headingNumber">2.2.1 </span><span class="head">Application Information</span></h3>
                              <p>It is
                                 sometimes convenient to store information relating to the processing of an encoded
                                 resource within its header. Typical uses for such information might be:
                              </p>
                              <ul>
                                 
                                 <li class="item">to allow an application to discover that it has previously opened or
                                    edited a file, and what version of itself was used to do that;
                                 </li>
                                 
                                 <li class="item">to show (through a date) which application last edited the file to
                                    allow for diagnosis of any problems that might have been caused by that
                                    application;
                                 </li>
                                 
                                 <li class="item">to allow users to discover information about an application used to
                                    edit the file
                                 </li>
                                 
                                 <li class="item">to allow the application to declare an interest in elements of the
                                    file which it has edited, so that other applications or human editors may be more
                                    wary of making changes to those sections of the file.
                                 </li>
                                 
                              </ul>
                              <ul class="specList">
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/application">application</a></span>
                                    Provides information about an application which has acted upon the current
                                    document.
                                    <table class="specDesc">
                                       
                                       <tr>
                                          
                                          <td class="Attribute"><span class="att">version</span></td>
                                          
                                          <td>supplies a version number for an application, independent of its identifier
                                             or display name.
                                          </td>
                                          
                                       </tr>
                                       
                                    </table>
                                 </li>
                                 
                              </ul>
                              <p>Each <a class="link_odd_elementSpec" href="/documentation/2.1.1/application">application</a> element identifies the current
                                 state of one software application with regard to the current file. This element is
                                 a
                                 member of the att.datable class, which provides a variety of attributes for
                                 associating this state with a date and time, or a temporal range. The <span class="att">xml:id</span> and <span class="att">version</span> attributes should be
                                 used to uniquely identify the application and its major version number (for example,
                                 'Edirom Tool 1.5'). It is not intended that a software application should add a new
                                 <a class="link_odd_elementSpec" href="/documentation/2.1.1/application">application</a> element each time it touches the
                                 file.
                              </p>
                              <p>The following example shows how these elements might be used to record the
                                 fact that version 1.5 of an application called ‘Music Markup Tool’ has an interest
                                 in
                                 two parts of a document. The parts concerned are accessible at the URLs given as
                                 targets of the two <a class="link_odd_elementSpec" href="/documentation/2.1.1/ptr">ptr</a> elements. When used on <a class="link_odd_elementSpec" href="/documentation/2.1.1/application">application</a>, the <span class="att">date</span> attribute
                                 specifies when the application was employed, in this case June 6, 2011. Version
                                 information for the application should be placed in <span class="att">version</span>.
                              </p>
                              <div id="index.xml-egXML-d39e3459" class="pre egXML_valid">
                                 <span data-indentation="1" class="element">&lt;appInfo&gt;</span><br />   <span data-indentation="2" class="element">&lt;application <span class="attribute">isodate</span>="<span class="attributevalue">2011-06-06</span>" <span class="attribute">version</span>="<span class="attributevalue">1.5</span>" <span class="attribute">xml:id</span>="<span class="attributevalue">header.MusicMarkupTool</span>"&gt;</span><br />     <span data-indentation="3" class="element">&lt;name&gt;</span>Music Markup Tool<span data-indentation="3" class="element">&lt;/name&gt;</span><br />
                                     <span data-indentation="3" class="element">&lt;ptr <span class="attribute">target</span>="<span class="attributevalue">#header.P1</span>"/&gt;</span><br />     <span data-indentation="3" class="element">&lt;ptr <span class="attribute">target</span>="<span class="attributevalue">#header.P2</span>"/&gt;</span><br />   <span data-indentation="2" class="element">&lt;/application&gt;</span><br />
                                 <span data-indentation="1" class="element">&lt;/appInfo&gt;</span>
                                 
                              </div>
                           </div>
                           <div class="div3" id="EditorialPrinciples">
                              <h3><span class="headingNumber">2.2.2 </span><span class="head">Declaration of Editorial
                                    Principles</span></h3>
                              <p>The <a class="link_odd_elementSpec" href="/documentation/2.1.1/editorialDecl">editorialDecl</a> element is
                                 used to provide details of the editorial practices applied during the encoding of
                                 a
                                 musical text.
                              </p>
                              <p>It may contain a prose description only, or one or more of a set
                                 of specialized elements; that is, members of the MEI model.editorialDeclPart class.
                                 
                              </p>
                              <p>Some of these policy elements carry attributes to support automated processing
                                 of certain well-defined editorial decisions; all of them contain a prose description
                                 of the editorial principles adopted with respect to the particular feature concerned.
                                 Examples of the kinds of questions which these descriptions are intended to answer
                                 are
                                 given in the list below.
                              </p>
                              <dl>
                                 
                                 <dt><span>correction</span></dt>
                                 
                                 <dd>
                                    <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/correction">correction</a></span>
                                       States how and under what circumstances corrections have been made in the
                                       text.
                                       <table class="specDesc">
                                          
                                          <tr>
                                             
                                             <td class="Attribute"><span class="att">corrlevel</span></td>
                                             
                                             <td>indicates the degree of correction applied to the text.</td>
                                             
                                          </tr>
                                          
                                       </table>
                                    </li>
                                    
                                    <li><span class="specList-classSpec"><a href="/documentation/2.1.1/att.regularmethod">att.regularmethod</a></span> Attributes that describe correction and
                                       normalization methods.
                                       <table class="specDesc">
                                          
                                          <tr>
                                             
                                             <td class="Attribute"><span class="att">method</span></td>
                                             
                                             <td>indicates the method employed to mark corrections and normalizations.</td>
                                             
                                          </tr>
                                          
                                       </table>
                                    </li>
                                    
                                    <p>Was the text corrected during or after data capture? If so, were corrections made
                                       silently or are they marked using the tags described in chapter <a class="link_ptr" href="/documentation/2.1.1/editTrans" title="0"><span class="headingNumber">11
                                             </span>Editorial Markup</a>? What principles have been adopted with respect to
                                       omissions, truncations, dubious corrections, alternate readings, false starts,
                                       repetitions, etc.?
                                    </p>
                                 </dd>
                                 
                                 <dt><span>interpretation</span></dt>
                                 
                                 <dd>
                                    <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/interpretation">interpretation</a></span> Describes the scope of any analytic or interpretive
                                       information added to the transcription of the music.
                                    </li>
                                    
                                    <p>Has any analytic or ‘interpretive’ information been provided — that is,
                                       information which is felt to be non-obvious, or potentially contentious? If so,
                                       how was it generated? How was it encoded?
                                    </p>
                                 </dd>
                                 
                                 <dt><span>normalization</span></dt>
                                 
                                 <dd>
                                    <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/normalization">normalization</a></span> Indicates the extent of normalization or
                                       regularization of the original source carried out in converting it to electronic
                                       form.
                                    </li>
                                    
                                    <li><span class="specList-classSpec"><a href="/documentation/2.1.1/att.regularmethod">att.regularmethod</a></span> Attributes that describe correction and
                                       normalization methods.
                                       <table class="specDesc">
                                          
                                          <tr>
                                             
                                             <td class="Attribute"><span class="att">method</span></td>
                                             
                                             <td>indicates the method employed to mark corrections and normalizations.</td>
                                             
                                          </tr>
                                          
                                       </table>
                                    </li>
                                    
                                    <p>Was the text normalized, for example by regularizing any non-standard enharmonic
                                       spellings, etc.? If so, were normalizations performed silently or are they marked
                                       using the tags described in chapter <a class="link_ptr" href="/documentation/2.1.1/editTrans" title="0"><span class="headingNumber">11 </span>Editorial Markup</a> ? What
                                       authority was used for the regularization? Also, what principles were used when
                                       normalizing numbers to provide the standard values for the <span class="att">value</span> attribute described in section <a class="link_ptr" href="/documentation/2.1.1/shared#namesNumbersDates" title="Names Dates Numbers Abbreviations and Addresses"><span class="headingNumber">1.3.4 </span>Names, Dates, Numbers, Abbreviations, and
                                          Addresses</a> and what format is used for them?
                                    </p>
                                 </dd>
                                 
                                 <dt><span>segmentation</span></dt>
                                 
                                 <dd>
                                    <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/segmentation">segmentation</a></span> Describes the principles according to which the musical
                                       text has been segmented, for example into movements, sections, etc.
                                    </li>
                                    
                                    <p>How is the musical text segmented? If mdiv and/or section elements have been used
                                       to partition the music for analysis, how are they marked and how was the
                                       segmentation arrived at?
                                    </p>
                                 </dd>
                                 
                                 <dt><span>standard values</span></dt>
                                 
                                 <dd>
                                    <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/stdVals">stdVals</a></span>
                                       (standard values) – Specifies the format used when standardized date or number
                                       values are supplied.
                                    </li>
                                    
                                    <p>In most cases, attributes bearing standardized values should conform to a defined
                                       datatype. In cases where this is not appropriate, this element may be used to
                                       describe the standardization methods underlying the values supplied.
                                    </p>
                                 </dd>
                                 
                              </dl>
                              <p>Experience shows that a full record should be kept of decisions relating to
                                 editorial principles and encoding practice, both for future users of the text and
                                 for
                                 the project which produced the text in the first instance. Any information about the
                                 editorial principles applied not falling under one of the above headings may be
                                 recorded as additional prose following the special-use elements.
                              </p>
                              <div id="index.xml-egXML-d39e3544" class="pre egXML_valid">
                                 <span data-indentation="1" class="element">&lt;editorialDecl&gt;</span><br />   <span data-indentation="2" class="element">&lt;segmentation&gt;</span><br />     <span data-indentation="3" class="element">&lt;p&gt;</span>Separate mdiv elements have been created for each movement of the work.<span data-indentation="3" class="element">&lt;/p&gt;</span><br />   <span data-indentation="2" class="element">&lt;/segmentation&gt;</span><br />   <span data-indentation="2" class="element">&lt;interpretation&gt;</span><br />
                                     <span data-indentation="3" class="element">&lt;p&gt;</span>The harmonic analysis applied throughout movement 1 was added by hand and has not
                                       been checked.<span data-indentation="3" class="element">&lt;/p&gt;</span><br />   <span data-indentation="2" class="element">&lt;/interpretation&gt;</span><br />   <span data-indentation="2" class="element">&lt;correction&gt;</span><br />
                                     <span data-indentation="3" class="element">&lt;p&gt;</span>Errors in transcription controlled by using the Finale editor.<span data-indentation="3" class="element">&lt;/p&gt;</span><br />   <span data-indentation="2" class="element">&lt;/correction&gt;</span><br />
                                   <span data-indentation="2" class="element">&lt;normalization&gt;</span><br />     <span data-indentation="3" class="element">&lt;p&gt;</span>All sung text converted to Modern American spelling following Webster’s 9th
                                       Collegiate dictionary.<span data-indentation="3" class="element">&lt;/p&gt;</span><br />   <span data-indentation="2" class="element">&lt;/normalization&gt;</span><br />   <span data-indentation="2" class="element">&lt;p/&gt;</span><br />
                                 <span data-indentation="1" class="element">&lt;/editorialDecl&gt;</span>
                                 
                              </div>
                              <p>An editorial practices declaration which applies to more than one text or
                                 division of a text need not be repeated in the header of each text or division.
                                 Instead, the <span class="att">decls</span> attribute of each text (or subdivision of
                                 the text) to which it applies may be used to supply a cross-reference to a single
                                 declaration encoded in the header.
                              </p>
                           </div>
                           <div class="div3" id="projectDescription">
                              <h3><span class="headingNumber">2.2.3 </span><span class="head">Project
                                    Description</span></h3>
                              <ul class="specList">
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/projectDesc">projectDesc</a></span>
                                    (project description) – Project-level meta-data describing the aim or purpose for
                                    which the electronic file was encoded, funding agencies, etc. together with any
                                    other relevant information concerning the process by which it was assembled or
                                    collected.
                                 </li>
                                 
                              </ul>
                              <p>The <a class="link_odd_elementSpec" href="/documentation/2.1.1/projectDesc">projectDesc</a> element may be used to describe,
                                 in prose, the purpose for which a digital resource was created, together with any
                                 other relevant information concerning the process by which it was assembled or
                                 collected. This is of particular importance for corpora or miscellaneous collections,
                                 but may be of use for any text, for example to explain why one kind of encoding
                                 practice has been followed rather than another.
                              </p>
                              <p>For example:</p>
                              <div id="index.xml-egXML-d39e3595" class="pre egXML_valid">
                                 <span data-indentation="1" class="element">&lt;encodingDesc&gt;</span><br />   <span data-indentation="2" class="element">&lt;projectDesc&gt;</span><br />     <span data-indentation="3" class="element">&lt;p&gt;</span>Texts collected for use in the MEI Summer Workshop, Aug. 2012.<span data-indentation="3" class="element">&lt;/p&gt;</span><br />   <span data-indentation="2" class="element">&lt;/projectDesc&gt;</span><br />
                                 <span data-indentation="1" class="element">&lt;/encodingDesc&gt;</span>
                                 
                              </div>
                           </div>
                           <div class="div3" id="samplingDeclaration">
                              <h3><span class="headingNumber">2.2.4 </span><span class="head">Sampling Declaration</span></h3>
                              <p>The samplingDecl
                                 element holds a prose description of the rationale and methods used in selecting
                                 texts, or parts of text, for inclusion in the resource.
                              </p>
                              <ul class="specList">
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/samplingDecl">samplingDecl</a></span>
                                    (sampling declaration) – Contains a prose description of the rationale and methods
                                    used in sampling texts in the creation of a corpus or collection.
                                 </li>
                                 
                              </ul>
                              <p>The <a class="link_odd_elementSpec" href="/documentation/2.1.1/samplingDecl">samplingDecl</a> element should include
                                 information about such matters as:
                              </p>
                              <ul>
                                 
                                 <li class="item">the size of individual samples</li>
                                 
                                 <li class="item">the method or methods by which they were selected</li>
                                 
                                 <li class="item">the underlying population being sampled</li>
                                 
                                 <li class="item">the object of the sampling procedure used</li>
                                 
                              </ul>
                              <p>but is not restricted to these.</p>
                              <div id="index.xml-egXML-d39e3632" class="pre egXML_valid">
                                 <span data-indentation="1" class="element">&lt;samplingDecl&gt;</span><br />   <span data-indentation="2" class="element">&lt;p&gt;</span>Encoding contains 40 randomly-selected measures.<span data-indentation="2" class="element">&lt;/p&gt;</span><br />
                                 <span data-indentation="1" class="element">&lt;/samplingDecl&gt;</span>
                                 
                              </div>
                              <p>It may also include a simple description of any parts of the source text
                                 included or excluded:
                              </p>
                              <div id="index.xml-egXML-d39e3642" class="pre egXML_valid">
                                 <span data-indentation="1" class="element">&lt;samplingDecl&gt;</span><br />   <span data-indentation="2" class="element">&lt;p&gt;</span><br />Only the songs have been transcribed. Advertisements have been silently omitted. All
                                     mathematical expressions have been omitted, and their place marked with a <span data-indentation="3" class="element">&lt;gi <span class="attribute">scheme</span>="<span class="attributevalue">MEI</span>"&gt;</span>gap<span data-indentation="3" class="element">&lt;/gi&gt;</span>     element.<span data-indentation="2" class="element">&lt;/p&gt;</span><br />
                                 <span data-indentation="1" class="element">&lt;/samplingDecl&gt;</span>
                                 
                              </div>
                              <div id="index.xml-egXML-d39e3653" class="pre egXML_valid">
                                 <span data-indentation="1" class="element">&lt;samplingDecl&gt;</span><br />   <span data-indentation="2" class="element">&lt;p&gt;</span>Only the first 6 measures of movement 1 are encoded.<span data-indentation="2" class="element">&lt;/p&gt;</span><br />
                                 <span data-indentation="1" class="element">&lt;/samplingDecl&gt;</span>
                                 
                              </div>
                              <p>A sampling declaration which applies to more than one text or division of a
                                 text need not be repeated in the header of each such text. Instead, the <span class="att">decls</span> attribute of each text (or subdivision of the text) to
                                 which the sampling declaration applies may be used to supply a cross-reference to
                                 it,
                                 as further described in section <a class="link_ptr" href="/documentation/2.1.1/header#associatingMetadataAndData" title="Associating Metadata and Data"><span class="headingNumber">2.1.7.1
                                       </span>Associating Metadata and Data</a>.
                              </p>
                           </div>
                        </div>
                        <div class="div2" id="workDescription">
                           <h2><span class="headingNumber">2.3 </span><span class="head">Work
                                 Description</span></h2>
                           <p>The <a class="link_odd_elementSpec" href="/documentation/2.1.1/workDesc">workDesc</a> element is the
                              third major subdivision of the MEI Header. It is an optional element, the purpose
                              of
                              which is to enable the recording of information characterizing various descriptive
                              aspects of the abstract work.
                           </p>
                           <ul class="specList">
                              
                              <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/workDesc">workDesc</a></span> (work
                                 description) – Grouping mechanism for information describing non-bibliographic aspects
                                 of a text.
                              </li>
                              
                              <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/work">work</a></span> Provides a
                                 detailed description of a work, specifically its history, language use, and high-level
                                 musical attributes: key, tempo, meter, and medium of performance.
                              </li>
                              
                           </ul>
                           <p>Within <a class="link_odd_elementSpec" href="/documentation/2.1.1/workDesc">workDesc</a>, the <a class="link_odd_elementSpec" href="/documentation/2.1.1/work">work</a> element is used to hold information for each resource being
                              described.
                           </p>
                           <ul class="specList">
                              
                              <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/work">work</a></span> Provides a
                                 detailed description of a work, specifically its history, language use, and high-level
                                 musical attributes: key, tempo, meter, and medium of performance.
                              </li>
                              
                           </ul>
                           <p>All the components of <a class="link_odd_elementSpec" href="/documentation/2.1.1/work">work</a> are optional, but they
                              must occur in the following order:
                           </p>
                           <ol>
                              
                              <li class="item">identifier</li>
                              
                              <li class="item">titleStmt</li>
                              
                              <li class="item">incip</li>
                              
                              <li class="item">key</li>
                              
                              <li class="item">mensuration</li>
                              
                              <li class="item">meter</li>
                              
                              <li class="item">tempo</li>
                              
                              <li class="item">otherChar</li>
                              
                              <li class="item">history</li>
                              
                              <li class="item">langUsage</li>
                              
                              <li class="item">perfMedium</li>
                              
                              <li class="item">audience</li>
                              
                              <li class="item">contents</li>
                              
                              <li class="item">context</li>
                              
                              <li class="item">biblList</li>
                              
                              <li class="item">notesStmt</li>
                              
                              <li class="item">classification</li>
                              
                           </ol>
                           <p>These work description components may be classed into two groups based on their
                              function: 
                           </p>
                           <ul>
                              
                              <li class="item">identification of the work: identifier, titleStmt, incip, key,
                                 mensuration, meter, tempo, otherChar
                              </li>
                              
                              <li class="item">contextual information for the work: history, langUsage, perfMedium,
                                 audience, contents, context, biblList, notesStmt, classification
                              </li>
                              
                           </ul>
                           <div class="div3" id="workIdentification">
                              <h3><span class="headingNumber">2.3.1
                                    </span><span class="head">Work Identification</span></h3>
                              <p>The following elements
                                 provide minimal identifying information for the intellectual work:
                              </p>
                              <ul class="specList">
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/identifier">identifier</a></span> An
                                    alpha-numeric string that establishes the identity of the described material.
                                 </li>
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/titleStmt">titleStmt</a></span>
                                    (title statement) – Container for title and responsibility meta-data.
                                 </li>
                                 
                              </ul>
                              <p>The identifier and title values recorded here may or may not be the same as
                                 those assigned to published versions of the work. Fuller details regarding the use
                                 of
                                 <a class="link_odd_elementSpec" href="/documentation/2.1.1/titleStmt">titleStmt</a> are available in section <a class="link_ptr" href="/documentation/2.1.1/header#titlestmt" title="Title Statement"><span class="headingNumber">2.1.1 </span>Title Statement</a>.
                              </p>
                           </div>
                           <div class="div3" id="workIncipit">
                              <h3><span class="headingNumber">2.3.2 </span><span class="head">Incipits</span></h3>
                              <ul class="specList">
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/incip">incip</a></span> (incipit) –
                                    The opening music and/or words of a composition.
                                 </li>
                                 
                              </ul>
                              <p>The first few notes and/or words of a piece of music are often used for
                                 identification purposes, especially when the piece has only a generic title, such
                                 as
                                 "Sonata no. 3". They appear in catalogs of music and in tables of contents of printed
                                 music that include multiple works.
                              </p>
                              <p>The following elements are provided for the
                                 inclusion of incipits:
                              </p>
                              <ul class="specList">
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/incip">incip</a></span> (incipit) –
                                    The opening music and/or words of a composition.
                                 </li>
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/incipCode">incipCode</a></span>
                                    Incipit coded in a non-XML, plain text format, such as Plaine &amp; Easie Code.
                                 </li>
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/incipText">incipText</a></span>
                                    Opening words of a musical composition.
                                 </li>
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/score">score</a></span> Full score
                                    view of the musical content.
                                 </li>
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/graphic">graphic</a></span> Indicates
                                    the location of an inline graphic, illustration, or figure.
                                 </li>
                                 
                              </ul>
                              <p>The elements <a class="link_odd_elementSpec" href="/documentation/2.1.1/incipCode">incipCode</a> and <a class="link_odd_elementSpec" href="/documentation/2.1.1/incipText">incipText</a> are available for the inclusion of coded incipits of music
                                 notation and textual incipits, respectively. The <a class="link_odd_elementSpec" href="/documentation/2.1.1/incipText">incipText</a> element should contain only the initial performed text of
                                 the work, while <a class="link_odd_elementSpec" href="/documentation/2.1.1/incipCode">incipCode</a> may contain both words and
                                 music, depending on the capabilities of the scheme used to encode it. When both music
                                 and text are provided in <a class="link_odd_elementSpec" href="/documentation/2.1.1/incipCode">incipCode</a>, it may be helpful
                                 to repeat the text in <a class="link_odd_elementSpec" href="/documentation/2.1.1/incipText">incipText</a> in order to provide
                                 easier access to only the text, for example, for indexing of the text without having
                                 to extract it from the coded incipit.
                              </p>
                              <p>Both <a class="link_odd_elementSpec" href="/documentation/2.1.1/incipCode">incipCode</a> and <a class="link_odd_elementSpec" href="/documentation/2.1.1/incipText">incipText</a> allow
                                 reference to an external file location via the <span class="att">target</span>
                                 attribute and specification of the internet media type of the external file via the
                                 <span class="att">mimetype</span> attribute. It is a semantic error not to include
                                 one of these attributes.
                              </p>
                              <p>An MEI-encoded incipit may be captured in the <a class="link_odd_elementSpec" href="/documentation/2.1.1/score">score</a> element.
                              </p>
                              <p>In addition, <a class="link_odd_elementSpec" href="/documentation/2.1.1/graphic">graphic</a> may be used to include an image of an incipit.
                              </p>
                           </div>
                           <div class="div3" id="workKeyTempoMeter">
                              <h3><span class="headingNumber">2.3.3 </span><span class="head">Key, Tempo, and Meter</span></h3>
                              <p>The attributes key, tempo, and
                                 meter are often helpful for identifying a musical work when it does not have a
                                 distinctive title.
                              </p>
                              <ul class="specList">
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/key">key</a></span> Key captures
                                    information about tonal center and mode.
                                 </li>
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/mensuration">mensuration</a></span>
                                    Captures information about mensuration within bibliographic descriptions.
                                 </li>
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/meter">meter</a></span> Captures
                                    information about the time signature within bibliographic descriptions.
                                 </li>
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/tempo">tempo</a></span> Text and
                                    symbols descriptive of tempo, mood, or style, e.g., "allarg.", "a tempo",
                                    "cantabile", "Moderato", "♩=60", "Moderato ♩ =60").
                                 </li>
                                 
                              </ul>
                              <p>The <a class="link_odd_elementSpec" href="/documentation/2.1.1/key">key</a> element is used exclusively within
                                 bibliographic descriptions. Do not confuse this element with <a class="link_odd_elementSpec" href="/documentation/2.1.1/keySig">keySig</a>, which is used within the body of an MEI file to record this
                                 data for musical notation. Likewise, <a class="link_odd_elementSpec" href="/documentation/2.1.1/meter">meter</a> should not
                                 be confused with the attributes used by staffDef and scoreDef to record meter-related
                                 data for notated music. The <a class="link_odd_elementSpec" href="/documentation/2.1.1/tempo">tempo</a> element can be used
                                 here as well as in the body of an MEI document; however, its attributes other than
                                 <span class="att">xml:id</span>, <span class="att">label</span>, <span class="att">n</span>, <span class="att">base</span>, and <span class="att">lang</span> are
                                 meaningless in the MEI header context, and therefore should be avoided within a work
                                 description. The <a class="link_odd_elementSpec" href="/documentation/2.1.1/mensuration">mensuration</a> element is available for
                                 the description of works in the mensural repertoire. When a work uses meter and
                                 mensural signs, both <a class="link_odd_elementSpec" href="/documentation/2.1.1/mensuration">mensuration</a> and <a class="link_odd_elementSpec" href="/documentation/2.1.1/meter">meter</a> elements may be used.
                              </p>
                           </div>
                           <div class="div3" id="workOtherChar">
                              <h3><span class="headingNumber">2.3.4 </span><span class="head">Other
                                    Identifying Characteristics</span></h3>
                              <p>Additional information that aids the
                                 identification of the work may be encoded using <a class="link_odd_elementSpec" href="/documentation/2.1.1/otherChar">otherChar</a>.
                              </p>
                              <p><span class="li" style="display:list-item"><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/otherChar">otherChar</a></span> (other
                                    distinguishing characteristic) – Any characteristic that serves to differentiate a
                                    work or expression from another.</span></p>
                              <p>The following components provide
                                 detailed information about the work's context, including the circumstances of its
                                 creation, the languages used within it, high-level musical attributes, performing
                                 forces, etc.
                              </p>
                           </div>
                           <div class="div3" id="workHistory">
                              <h3><span class="headingNumber">2.3.5 </span><span class="head">Work History</span></h3>
                              <p>The
                                 following elements are provided to capture the history of a musical work:
                              </p>
                              <ul class="specList">
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/history">history</a></span> Provides
                                    a container for information about the creation and history of a resource.
                                 </li>
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/creation">creation</a></span>
                                    Non-bibliographic details of the creation of an intellectual entity, in narrative
                                    form, such as the date, place, and circumstances of its composition.
                                 </li>
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/eventList">eventList</a></span>
                                    Contains historical information given as a sequence of significant past events.
                                 </li>
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/event">event</a></span> Contains a
                                    description of an event, including the dates and locations of its occurrence and
                                    prominent participants.
                                 </li>
                                 
                              </ul>
                              <p>The <a class="link_odd_elementSpec" href="/documentation/2.1.1/history">history</a> element is a container for the
                                 non-bibliographic details relating to a work. The <a class="link_odd_elementSpec" href="/documentation/2.1.1/creation">creation</a> element is intended to contain a brief statement of the
                                 circumstances of the work's creation. Its content is limited to text and <a class="link_odd_elementSpec" href="/documentation/2.1.1/date">date</a> and <a class="link_odd_elementSpec" href="/documentation/2.1.1/geogName">geogName</a>
                                 elements. Following it, a list of key events in the creation of the work may be
                                 enumerated using <a class="link_odd_elementSpec" href="/documentation/2.1.1/eventList">eventList</a>. The list is comprised of
                                 <a class="link_odd_elementSpec" href="/documentation/2.1.1/event">event</a> elements that contain a brief description of
                                 the associated event, including dates and locations where the event took place. The
                                 <span class="att">type</span> attribute may be used to distinguish between multiple
                                 event lists with different functions, such as a list of events in the compositional
                                 process and a list of performance dates.
                              </p>
                              <p>Paragraphs may be mixed with event
                                 lists, or used instead of <a class="link_odd_elementSpec" href="/documentation/2.1.1/eventList">eventList</a> and <a class="link_odd_elementSpec" href="/documentation/2.1.1/creation">creation</a> elements, when a fuller, 'essay-like' description
                                 is desired.
                              </p>
                           </div>
                           <div class="div3" id="workLanguage">
                              <h3><span class="headingNumber">2.3.6 </span><span class="head">Language
                                    Usage</span></h3>
                              <p>The <a class="link_odd_elementSpec" href="/documentation/2.1.1/langUsage">langUsage</a> element is used
                                 within the <a class="link_odd_elementSpec" href="/documentation/2.1.1/workDesc">workDesc</a> element to describe the languages,
                                 sublanguages, dialects, etc. represented within a work. It contains one or more <a class="link_odd_elementSpec" href="/documentation/2.1.1/language">language</a> elements, each of which provides information
                                 about a single language.
                              </p>
                              <ul class="specList">
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/langUsage">langUsage</a></span>
                                    (language usage) – Groups elements describing the languages, sub-languages,
                                    dialects, etc., represented within the encoded resource.
                                 </li>
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/language">language</a></span>
                                    Description of a language used in the document.
                                 </li>
                                 
                              </ul>
                              <p>A <a class="link_odd_elementSpec" href="/documentation/2.1.1/language">language</a> element may be supplied for each
                                 different language used in a document. If used, its <span class="att">xml:id</span>
                                 attribute should specify an appropriate language identifier. This is particularly
                                 important if extended language identifiers have been used as the value of @xml:lang
                                 attributes elsewhere in the document.
                              </p>
                              <p>Here is an example of the use of this
                                 element:
                              </p>
                              <div id="index.xml-egXML-d39e3971" class="pre egXML_valid">
                                 <span data-indentation="1" class="element">&lt;langUsage&gt;</span><br />   <span data-indentation="2" class="element">&lt;language <span class="attribute">xml:id</span>="<span class="attributevalue">fr-CA</span>"&gt;</span>Québecois<span data-indentation="2" class="element">&lt;/language&gt;</span><br />
                                   <span data-indentation="2" class="element">&lt;language <span class="attribute">xml:id</span>="<span class="attributevalue">en-CA</span>"&gt;</span>Canadian English<span data-indentation="2" class="element">&lt;/language&gt;</span><br />   <span data-indentation="2" class="element">&lt;language <span class="attribute">xml:id</span>="<span class="attributevalue">en-GB</span>"&gt;</span>British English<span data-indentation="2" class="element">&lt;/language&gt;</span><br />
                                 <span data-indentation="1" class="element">&lt;/langUsage&gt;</span><br />
                                 <span data-indentation="1" class="element">&lt;verse <span class="attribute">n</span>="<span class="attributevalue">1</span>" <span class="attribute">xml:lang</span>="<span class="attributevalue">fr-CA</span>"/&gt;</span><br />
                                 <span data-indentation="1" class="element">&lt;verse <span class="attribute">n</span>="<span class="attributevalue">2</span>" <span class="attribute">xml:lang</span>="<span class="attributevalue">en-CA</span>"/&gt;</span><br />
                                 <span data-indentation="1" class="element">&lt;verse <span class="attribute">n</span>="<span class="attributevalue">3</span>" <span class="attribute">xml:lang</span>="<span class="attributevalue">en-GB</span>"/&gt;</span>
                                 
                              </div>
                           </div>
                           <div class="div3" id="workMedium">
                              <h3><span class="headingNumber">2.3.7
                                    </span><span class="head">Performance Medium</span></h3>
                              <p>The following elements
                                 are available for description of a composition's performing forces:
                              </p>
                              <ul class="specList">
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/perfMedium">perfMedium</a></span>
                                    (performance medium) – Indicates the number and character of the performing forces
                                    used in a musical composition.
                                 </li>
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/castList">castList</a></span>
                                    Contains a single cast list or dramatis personae.
                                 </li>
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/instrumentation">instrumentation</a></span> Instrumental and non-dramatic vocal resources.
                                 </li>
                                 
                              </ul>
                              <p>The <a class="link_odd_elementSpec" href="/documentation/2.1.1/perfMedium">perfMedium</a> element provides the possibility
                                 of describing a work in terms of its medium of performance; that is, the performing
                                 forces required. In the case of a dramatic work, the dramatis personae and associated
                                 voice qualities may be enumerated using <a class="link_odd_elementSpec" href="/documentation/2.1.1/castList">castList</a>. The
                                 <a class="link_odd_elementSpec" href="/documentation/2.1.1/instrumentation">instrumentation</a> element describes the necessary
                                 instrumental resources.
                              </p>
                              <div class="div4" id="workCast">
                                 <h4><span class="headingNumber">2.3.7.1 </span><span class="head">Cast Lists</span></h4>
                                 <p>A
                                    cast list is a specialized form of list, conventionally found at the start or end
                                    of
                                    a dramatic work, usually listing all the speaking/singing and non-speaking/singing
                                    roles in the play, often with additional description (‘Cataplasma, a maker of
                                    Periwigges and Attires’) or the name of an actor or actress (‘Old Lady Squeamish.
                                    Mrs Rutter’).
                                 </p>
                                 <ul class="specList">
                                    
                                    <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/castList">castList</a></span>
                                       Contains a single cast list or dramatis personae.
                                    </li>
                                    
                                    <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/castItem">castItem</a></span>
                                       Contains a single entry within a cast list, describing either a single role or a
                                       list of non-speaking roles.
                                    </li>
                                    
                                    <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/castGrp">castGrp</a></span> (cast
                                       group) – Groups one or more individual castItem elements within a cast list.
                                    </li>
                                    
                                 </ul>
                                 <p>Cast lists often function as identifying metadata and for this reason are
                                    permitted within the description of a work.
                                 </p>
                                 <p>Because the format and internal
                                    structure of cast lists are unpredictable, a <a class="link_odd_elementSpec" href="/documentation/2.1.1/castList">castList</a> may contain any combination of <a class="link_odd_elementSpec" href="/documentation/2.1.1/castItem">castItem</a> and <a class="link_odd_elementSpec" href="/documentation/2.1.1/castGrp">castGrp</a>
                                    elements.
                                 </p>
                                 <p>A <a class="link_odd_elementSpec" href="/documentation/2.1.1/castItem">castItem</a> element may contain any
                                    mixture of text and the following elements:
                                 </p>
                                 <ul class="specList">
                                    
                                    <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/role">role</a></span> Name of a
                                       dramatic role, as given in a cast list.
                                    </li>
                                    
                                    <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/roleDesc">roleDesc</a></span> (role
                                       description) – Describes a character's role in a drama.
                                    </li>
                                    
                                    <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/instrVoice">instrVoice</a></span>
                                       (instrument or voice) – Name of an instrument on which a performer plays or a
                                       performer's voice range.
                                    </li>
                                    
                                 </ul>
                                 <p>In the following example, <a class="link_odd_elementSpec" href="/documentation/2.1.1/role">role</a> provides the
                                    name of the dramatic character and <a class="link_odd_elementSpec" href="/documentation/2.1.1/roleDesc">roleDesc</a> contains
                                    a brief description of the role. The <a class="link_odd_elementSpec" href="/documentation/2.1.1/instrVoice">instrVoice</a>
                                    element is used to describe the voice range of the role.
                                 </p>
                                 <div id="index.xml-egXML-d39e4062" class="pre egXML_valid">
                                    <span data-indentation="1" class="element">&lt;castList&gt;</span><br />   <span data-indentation="2" class="element">&lt;castItem&gt;</span><br />     <span data-indentation="3" class="element">&lt;role&gt;</span>Ursula<span data-indentation="3" class="element">&lt;/role&gt;</span><br />     <span data-indentation="3" class="element">&lt;roleDesc&gt;</span>Queen of the Britons<span data-indentation="3" class="element">&lt;/roleDesc&gt;</span><br />     <span data-indentation="3" class="element">&lt;instrVoice&gt;</span>Soprano<span data-indentation="3" class="element">&lt;/instrVoice&gt;</span><br />
                                      <span data-indentation="2" class="element">&lt;/castItem&gt;</span><br />   <span data-indentation="2" class="element">&lt;castItem&gt;</span><br />     <span data-indentation="3" class="element">&lt;role&gt;</span>Dersagrena<span data-indentation="3" class="element">&lt;/role&gt;</span><br />     <span data-indentation="3" class="element">&lt;roleDesc&gt;</span>Handmaiden to Ursula<span data-indentation="3" class="element">&lt;/roleDesc&gt;</span><br />     <span data-indentation="3" class="element">&lt;instrVoice&gt;</span>Mezzo-Soprano<span data-indentation="3" class="element">&lt;/instrVoice&gt;</span><br />   <span data-indentation="2" class="element">&lt;/castItem&gt;</span><br />
                                      <span data-indentation="2" class="element">&lt;castItem&gt;</span><br />     <span data-indentation="3" class="element">&lt;role&gt;</span>Fingal<span data-indentation="3" class="element">&lt;/role&gt;</span><br />     <span data-indentation="3" class="element">&lt;roleDesc&gt;</span>King of the Britons<span data-indentation="3" class="element">&lt;/roleDesc&gt;</span><br />     <span data-indentation="3" class="element">&lt;instrVoice&gt;</span>Baritone<span data-indentation="3" class="element">&lt;/instrVoice&gt;</span><br />
                                      <span data-indentation="2" class="element">&lt;/castItem&gt;</span><br />
                                    <span data-indentation="1" class="element">&lt;/castList&gt;</span>
                                    
                                 </div>
                                 <p>The vocal qualities and associated roles for Beethoven's opera <span class="titlem">Fidelio</span> may be encoded as:
                                 </p>
                                 <div id="index.xml-egXML-d39e4108" class="pre egXML_valid">
                                    <span data-indentation="1" class="element">&lt;perfMedium&gt;</span><br />   <span data-indentation="2" class="element">&lt;castList&gt;</span><br />     <span data-indentation="3" class="element">&lt;castItem&gt;</span><br />
                                          <span data-indentation="4" class="element">&lt;instrVoice&gt;</span>Tenor<span data-indentation="4" class="element">&lt;/instrVoice&gt;</span><br />       <span data-indentation="4" class="element">&lt;role&gt;</span>Florestan<span data-indentation="4" class="element">&lt;/role&gt;</span><br />     <span data-indentation="3" class="element">&lt;/castItem&gt;</span><br />     <span data-indentation="3" class="element">&lt;castItem&gt;</span><br />       <span data-indentation="4" class="element">&lt;instrVoice&gt;</span>Soprano<span data-indentation="4" class="element">&lt;/instrVoice&gt;</span><br />
                                          <span data-indentation="4" class="element">&lt;role&gt;</span>Leonore<span data-indentation="4" class="element">&lt;/role&gt;</span><br />, <span data-indentation="4" class="element">&lt;roleDesc&gt;</span>his wife<span data-indentation="4" class="element">&lt;/roleDesc&gt;</span><br />     <span data-indentation="3" class="element">&lt;/castItem&gt;</span><br />     <span data-indentation="3" class="element">&lt;castItem&gt;</span><br />
                                          <span data-indentation="4" class="element">&lt;instrVoice&gt;</span>Bass<span data-indentation="4" class="element">&lt;/instrVoice&gt;</span><br />       <span data-indentation="4" class="element">&lt;role&gt;</span>Rocco<span data-indentation="4" class="element">&lt;/role&gt;</span><br />, <span data-indentation="4" class="element">&lt;roleDesc&gt;</span>gaoler<span data-indentation="4" class="element">&lt;/roleDesc&gt;</span><br />     <span data-indentation="3" class="element">&lt;/castItem&gt;</span><br />
                                        <span data-indentation="3" class="element">&lt;castItem&gt;</span><br />       <span data-indentation="4" class="element">&lt;instrVoice&gt;</span>Soprano<span data-indentation="4" class="element">&lt;/instrVoice&gt;</span><br />
                                          <span data-indentation="4" class="element">&lt;role&gt;</span>Marzelline<span data-indentation="4" class="element">&lt;/role&gt;</span><br />, <span data-indentation="4" class="element">&lt;roleDesc&gt;</span>his daughter<span data-indentation="4" class="element">&lt;/roleDesc&gt;</span><br />
                                        <span data-indentation="3" class="element">&lt;/castItem&gt;</span><br />     <span data-indentation="3" class="element">&lt;castItem&gt;</span><br />       <span data-indentation="4" class="element">&lt;instrVoice&gt;</span>Tenor<span data-indentation="4" class="element">&lt;/instrVoice&gt;</span><br />
                                          <span data-indentation="4" class="element">&lt;role&gt;</span>Jaquino<span data-indentation="4" class="element">&lt;/role&gt;</span><br />, <span data-indentation="4" class="element">&lt;roleDesc&gt;</span>assistant to Rocco<span data-indentation="4" class="element">&lt;/roleDesc&gt;</span><br />     <span data-indentation="3" class="element">&lt;/castItem&gt;</span><br />
                                        <span data-indentation="3" class="element">&lt;castItem&gt;</span><br />       <span data-indentation="4" class="element">&lt;instrVoice&gt;</span>Bass-baritone<span data-indentation="4" class="element">&lt;/instrVoice&gt;</span><br />       <span data-indentation="4" class="element">&lt;role&gt;</span>Don Pizarro<span data-indentation="4" class="element">&lt;/role&gt;</span><br />, <span data-indentation="4" class="element">&lt;roleDesc&gt;</span>governor of the prison<span data-indentation="4" class="element">&lt;/roleDesc&gt;</span><br />     <span data-indentation="3" class="element">&lt;/castItem&gt;</span><br />
                                        <span data-indentation="3" class="element">&lt;castItem&gt;</span><br />       <span data-indentation="4" class="element">&lt;instrVoice&gt;</span>Bass<span data-indentation="4" class="element">&lt;/instrVoice&gt;</span><br />
                                          <span data-indentation="4" class="element">&lt;role&gt;</span>Don Fernando<span data-indentation="4" class="element">&lt;/role&gt;</span><br />, <span data-indentation="4" class="element">&lt;roleDesc&gt;</span>King's minister<span data-indentation="4" class="element">&lt;/roleDesc&gt;</span><br />     <span data-indentation="3" class="element">&lt;/castItem&gt;</span><br />
                                      <span data-indentation="2" class="element">&lt;/castList&gt;</span><br />
                                    <span data-indentation="1" class="element">&lt;/perfMedium&gt;</span>
                                    
                                 </div>
                                 <p>The <a class="link_odd_elementSpec" href="/documentation/2.1.1/castItem">castItem</a> element may also contain:
                                 </p>
                                 <ul class="specList">
                                    
                                    <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/actor">actor</a></span> Name of an
                                       actor appearing within a cast list.
                                    </li>
                                    
                                 </ul>
                                 <p>However, this element is unlikely to be useful in the context of a work
                                    description. It may be used here, however, for the very rare occasion when a work
                                    was conceived for and is only performable by a single person or group, as for
                                    certain "performance art" works.
                                 </p>
                                 <p>It is common to find some roles presented in
                                    groups or sublists. Roles are also often grouped together by their function. To
                                    accommodate these situations, the <a class="link_odd_elementSpec" href="/documentation/2.1.1/castGrp">castGrp</a> element is
                                    provided as a component of <a class="link_odd_elementSpec" href="/documentation/2.1.1/castList">castList</a>. It may contain
                                    any combination of <a class="link_odd_elementSpec" href="/documentation/2.1.1/castItem">castItem</a>, <a class="link_odd_elementSpec" href="/documentation/2.1.1/castGrp">castGrp</a>, and <a class="link_odd_elementSpec" href="/documentation/2.1.1/roleDesc">roleDesc</a>
                                    elements.
                                 </p>
                              </div>
                              <div class="div4" id="workInstrumentation">
                                 <h4><span class="headingNumber">2.3.7.2 </span><span class="head">Instrumentation</span></h4>
                                 <p>The <a class="link_odd_elementSpec" href="/documentation/2.1.1/instrumentation">instrumentation</a>
                                    element is used to capture the solo and ensemble instrumental resources of a
                                    composition. For example, a work for a standard ensemble may be indicated
                                    thus:
                                 </p>
                                 <div id="index.xml-egXML-d39e4236" class="pre egXML_valid">
                                    <span data-indentation="1" class="element">&lt;perfMedium&gt;</span><br />   <span data-indentation="2" class="element">&lt;instrumentation&gt;</span><br />     <span data-indentation="3" class="element">&lt;ensemble&gt;</span>Orchestra<span data-indentation="3" class="element">&lt;/ensemble&gt;</span><br />
                                      <span data-indentation="2" class="element">&lt;/instrumentation&gt;</span><br />
                                    <span data-indentation="1" class="element">&lt;/perfMedium&gt;</span>
                                    
                                 </div>
                                 <p>The make-up of standard and non-standard ensembles may be enumerated using
                                    the <a class="link_odd_elementSpec" href="/documentation/2.1.1/instrVoice">instrVoice</a> element:
                                 </p>
                                 <div id="index.xml-egXML-d39e4252" class="pre egXML_valid">
                                    <span data-indentation="1" class="element">&lt;perfMedium&gt;</span><br />   <span data-indentation="2" class="element">&lt;instrumentation&gt;</span><br />     <span data-indentation="3" class="element">&lt;head&gt;</span>Orchestration<span data-indentation="3" class="element">&lt;/head&gt;</span><br />
                                        <span data-indentation="3" class="element">&lt;instrVoice&gt;</span>Flute<span data-indentation="3" class="element">&lt;/instrVoice&gt;</span><br />     <span data-indentation="3" class="element">&lt;instrVoice&gt;</span>Oboe<span data-indentation="3" class="element">&lt;/instrVoice&gt;</span><br />
                                        <span data-indentation="3" class="element">&lt;instrVoice&gt;</span>English Horn<span data-indentation="3" class="element">&lt;/instrVoice&gt;</span><br />     <span data-indentation="3" class="element">&lt;instrVoice&gt;</span>2 Horns in D<span data-indentation="3" class="element">&lt;/instrVoice&gt;</span><br />     <span data-indentation="3" class="element">&lt;instrVoice&gt;</span>Strings<span data-indentation="3" class="element">&lt;/instrVoice&gt;</span><br />
                                      <span data-indentation="2" class="element">&lt;/instrumentation&gt;</span><br />
                                    <span data-indentation="1" class="element">&lt;/perfMedium&gt;</span>
                                    
                                 </div>
                                 <p>Where multiple instruments of the same kind are used, the <span class="att">count</span> attribute on <a class="link_odd_elementSpec" href="/documentation/2.1.1/instrVoice">instrVoice</a> may be used
                                    to encode the exact number of players called for.
                                 </p>
                                 <div id="index.xml-egXML-d39e4287" class="pre egXML_valid">
                                    <span data-indentation="1" class="element">&lt;perfMedium&gt;</span><br />   <span data-indentation="2" class="element">&lt;instrumentation&gt;</span><br />          <span data-indentation="3" class="element">&lt;instrVoice <span class="attribute">count</span>="<span class="attributevalue">2</span>"&gt;</span>Piccolo<span data-indentation="3" class="element">&lt;/instrVoice&gt;</span><br />     <span data-indentation="3" class="element">&lt;instrVoice <span class="attribute">count</span>="<span class="attributevalue">2</span>"&gt;</span>Flute<span data-indentation="3" class="element">&lt;/instrVoice&gt;</span><br />
                                        <span data-indentation="3" class="element">&lt;instrVoice <span class="attribute">count</span>="<span class="attributevalue">3</span>"&gt;</span>1st Clarinet<span data-indentation="3" class="element">&lt;/instrVoice&gt;</span><br />
                                        <span data-indentation="3" class="element">&lt;instrVoice <span class="attribute">count</span>="<span class="attributevalue">3</span>"&gt;</span>2nd Clarinet<span data-indentation="3" class="element">&lt;/instrVoice&gt;</span><br />
                                        <span data-indentation="3" class="element">&lt;instrVoice <span class="attribute">count</span>="<span class="attributevalue">3</span>"&gt;</span>3rd Clarinet<span data-indentation="3" class="element">&lt;/instrVoice&gt;</span><br />
                                           <span data-indentation="2" class="element">&lt;/instrumentation&gt;</span><br />
                                    <span data-indentation="1" class="element">&lt;/perfMedium&gt;</span>
                                    
                                 </div>
                                 <p>Instrument or voice specifications may be grouped using the <a class="link_odd_elementSpec" href="/documentation/2.1.1/instrVoiceGrp">instrVoiceGrp</a> element and a label assigned to the group with <a class="link_odd_elementSpec" href="/documentation/2.1.1/head">head</a>. For example:
                                 </p>
                                 <div id="index.xml-egXML-d39e4318" class="pre egXML_valid">
                                    <span data-indentation="1" class="element">&lt;perfMedium&gt;</span><br />   <span data-indentation="2" class="element">&lt;instrumentation&gt;</span><br />          <span data-indentation="3" class="element">&lt;instrVoiceGrp&gt;</span><br />       <span data-indentation="4" class="element">&lt;head&gt;</span>Woodwinds<span data-indentation="4" class="element">&lt;/head&gt;</span><br />
                                          <span data-indentation="4" class="element">&lt;instrVoice <span class="attribute">count</span>="<span class="attributevalue">2</span>"&gt;</span>Piccolo<span data-indentation="4" class="element">&lt;/instrVoice&gt;</span><br />       <span data-indentation="4" class="element">&lt;instrVoice <span class="attribute">count</span>="<span class="attributevalue">2</span>"&gt;</span>Flute<span data-indentation="4" class="element">&lt;/instrVoice&gt;</span><br />       <span data-indentation="4" class="element">&lt;instrVoice <span class="attribute">count</span>="<span class="attributevalue">3</span>"&gt;</span>1st Clarinet<span data-indentation="4" class="element">&lt;/instrVoice&gt;</span><br />
                                          <span data-indentation="4" class="element">&lt;instrVoice <span class="attribute">count</span>="<span class="attributevalue">3</span>"&gt;</span>2nd Clarinet<span data-indentation="4" class="element">&lt;/instrVoice&gt;</span><br />
                                          <span data-indentation="4" class="element">&lt;instrVoice <span class="attribute">count</span>="<span class="attributevalue">3</span>"&gt;</span>3rd Clarinet<span data-indentation="4" class="element">&lt;/instrVoice&gt;</span><br />
                                               <span data-indentation="3" class="element">&lt;/instrVoiceGrp&gt;</span><br />     <span data-indentation="3" class="element">&lt;instrVoiceGrp&gt;</span><br />       <span data-indentation="4" class="element">&lt;head&gt;</span>Brass<span data-indentation="4" class="element">&lt;/head&gt;</span><br />       <span data-indentation="4" class="element">&lt;instrVoice <span class="attribute">count</span>="<span class="attributevalue">3</span>"&gt;</span>1st Trumpet<span data-indentation="4" class="element">&lt;/instrVoice&gt;</span><br />       <span data-indentation="4" class="element">&lt;instrVoice <span class="attribute">count</span>="<span class="attributevalue">3</span>"&gt;</span>2nd Trumpet<span data-indentation="4" class="element">&lt;/instrVoice&gt;</span><br />
                                          <span data-indentation="4" class="element">&lt;instrVoice <span class="attribute">count</span>="<span class="attributevalue">3</span>"&gt;</span>3rd Trumpet<span data-indentation="4" class="element">&lt;/instrVoice&gt;</span><br />       <span data-indentation="4" class="element">&lt;instrVoice <span class="attribute">count</span>="<span class="attributevalue">3</span>"&gt;</span>2nd Clarinet<span data-indentation="4" class="element">&lt;/instrVoice&gt;</span><br />            <span data-indentation="3" class="element">&lt;/instrVoiceGrp&gt;</span><br />        <span data-indentation="2" class="element">&lt;/instrumentation&gt;</span><br />
                                    <span data-indentation="1" class="element">&lt;/perfMedium&gt;</span>
                                    
                                 </div>
                                 <div id="index.xml-egXML-d39e4366" class="pre egXML_valid">
                                    <span data-indentation="1" class="element">&lt;perfMedium&gt;</span><br />   <span data-indentation="2" class="element">&lt;instrumentation&gt;</span><br />     <span data-indentation="3" class="element">&lt;instrVoiceGrp&gt;</span><br />       <span data-indentation="4" class="element">&lt;head&gt;</span>Woodwinds<span data-indentation="4" class="element">&lt;/head&gt;</span><br />
                                          <span data-indentation="4" class="element">&lt;instrVoice <span class="attribute">code</span>="<span class="attributevalue">wa</span>" <span class="attribute">count</span>="<span class="attributevalue">2</span>"&gt;</span><br />2 Flutes <span data-indentation="5" class="element">&lt;instrVoice <span class="attribute">code</span>="<span class="attributevalue">wz</span>"&gt;</span>(2.           piccolo)<span data-indentation="5" class="element">&lt;/instrVoice&gt;</span><br /><span data-indentation="4" class="element">&lt;/instrVoice&gt;</span><br />       <span data-indentation="4" class="element">&lt;instrVoice <span class="attribute">code</span>="<span class="attributevalue">wc</span>" <span class="attribute">count</span>="<span class="attributevalue">1</span>"&gt;</span>1 Oboe<span data-indentation="4" class="element">&lt;/instrVoice&gt;</span><br />       
                                        <span data-indentation="3" class="element">&lt;/instrVoiceGrp&gt;</span><br />     <span data-indentation="3" class="element">&lt;instrVoiceGrp&gt;</span><br />       <span data-indentation="4" class="element">&lt;head&gt;</span>Strings (8-6-4-4-2)<span data-indentation="4" class="element">&lt;/head&gt;</span><br />
                                          <span data-indentation="4" class="element">&lt;instrVoice <span class="attribute">count</span>="<span class="attributevalue">8</span>"&gt;</span>Violin 1<span data-indentation="4" class="element">&lt;/instrVoice&gt;</span><br />       <span data-indentation="4" class="element">&lt;instrVoice <span class="attribute">count</span>="<span class="attributevalue">6</span>"&gt;</span>Violin 2<span data-indentation="4" class="element">&lt;/instrVoice&gt;</span><br />       <span data-indentation="4" class="element">&lt;instrVoice <span class="attribute">count</span>="<span class="attributevalue">4</span>"&gt;</span>Viola<span data-indentation="4" class="element">&lt;/instrVoice&gt;</span><br />
                                          <span data-indentation="4" class="element">&lt;instrVoice <span class="attribute">count</span>="<span class="attributevalue">4</span>"&gt;</span>Violoncello<span data-indentation="4" class="element">&lt;/instrVoice&gt;</span><br />       <span data-indentation="4" class="element">&lt;instrVoice <span class="attribute">count</span>="<span class="attributevalue">2</span>"&gt;</span>Double Bass<span data-indentation="4" class="element">&lt;/instrVoice&gt;</span><br />     <span data-indentation="3" class="element">&lt;/instrVoiceGrp&gt;</span><br />   <span data-indentation="2" class="element">&lt;/instrumentation&gt;</span><br />
                                    <span data-indentation="1" class="element">&lt;/perfMedium&gt;</span>
                                    
                                 </div>
                                 <p>The preceding example also demonstrates how instrumental doublings can be
                                    accommodate through the use of nested <a class="link_odd_elementSpec" href="/documentation/2.1.1/instrVoice">instrVoice</a>
                                    elements.
                                 </p>
                                 <p>Both <a class="link_odd_elementSpec" href="/documentation/2.1.1/ensemble">ensemble</a> and <a class="link_odd_elementSpec" href="/documentation/2.1.1/instrVoice">instrVoice</a> provide the <span class="att">code</span> attribute,
                                    which can be used to record a coded value that represents the string value stored
                                    as
                                    the element's content. It is recommended that coded values be taken from a
                                    standardized list, such as the International Association of Music Libraries' Medium
                                    of performance Codes List or the MARC Instruments and Voices Code List.
                                 </p>
                                 <div id="index.xml-egXML-d39e4427" class="pre egXML_valid">
                                    <span data-indentation="1" class="element">&lt;perfMedium&gt;</span><br />   <span data-indentation="2" class="element">&lt;instrumentation&gt;</span><br />          <span data-indentation="3" class="element">&lt;instrVoice <span class="attribute">code</span>="<span class="attributevalue">ba</span>"&gt;</span>Horn<span data-indentation="3" class="element">&lt;/instrVoice&gt;</span><br />     <span data-indentation="3" class="element">&lt;instrVoice <span class="attribute">code</span>="<span class="attributevalue">bb</span>"&gt;</span>Trumpet<span data-indentation="3" class="element">&lt;/instrVoice&gt;</span><br />
                                        <span data-indentation="3" class="element">&lt;instrVoice <span class="attribute">code</span>="<span class="attributevalue">bd</span>"&gt;</span>Trombone<span data-indentation="3" class="element">&lt;/instrVoice&gt;</span><br />   <span data-indentation="2" class="element">&lt;/instrumentation&gt;</span><br />
                                    <span data-indentation="1" class="element">&lt;/perfMedium&gt;</span>
                                    
                                 </div>
                                 <p>Solo parts may be marked with the <span class="att">solo</span> attribute of
                                    <a class="link_odd_elementSpec" href="/documentation/2.1.1/instrVoice">instrVoice</a>, like so:
                                 </p>
                                 <div id="index.xml-egXML-d39e4452" class="pre egXML_valid">
                                    <span data-indentation="1" class="element">&lt;instrumentation&gt;</span><br />   <span data-indentation="2" class="element">&lt;instrVoice <span class="attribute">solo</span>="<span class="attributevalue">true</span>"&gt;</span>Violin<span data-indentation="2" class="element">&lt;/instrVoice&gt;</span><br />   <span data-indentation="2" class="element">&lt;instrVoice&gt;</span>Violin<span data-indentation="2" class="element">&lt;/instrVoice&gt;</span><br />
                                      <span data-indentation="2" class="element">&lt;instrVoice&gt;</span>Violin<span data-indentation="2" class="element">&lt;/instrVoice&gt;</span><br />   <span data-indentation="2" class="element">&lt;instrVoice&gt;</span>Viola<span data-indentation="2" class="element">&lt;/instrVoice&gt;</span><br />
                                      <span data-indentation="2" class="element">&lt;instrVoice&gt;</span>Violoncello<span data-indentation="2" class="element">&lt;/instrVoice&gt;</span><br />
                                    <span data-indentation="1" class="element">&lt;/instrumentation&gt;</span>
                                    
                                 </div>
                                 <p>Music for a single player should, however, never use the <span class="att">solo</span> attribute.
                                 </p>
                                 <div id="index.xml-egXML-d39e4477" class="pre egXML_valid">
                                    <span data-indentation="1" class="element">&lt;instrumentation&gt;</span><br />   <span data-indentation="2" class="element">&lt;instrVoice <span class="attribute">solo</span>="<span class="attributevalue">true</span>"&gt;</span>Piano<span data-indentation="2" class="element">&lt;/instrVoice&gt;</span><br />
                                    <span data-indentation="1" class="element">&lt;/instrumentation&gt;</span>
                                    
                                 </div>
                              </div>
                           </div>
                           <div class="teidiv2" id="workAudience">
                              <h3><span class="headingNumber">2.3.8 </span><span class="head">Audience and
                                    Context</span></h3>
                              <ul class="specList">
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/audience">audience</a></span> Defines
                                    the class of user for which the work is intended, as defined by age group (e.g.,
                                    children, young adults, adults, etc.), educational level (e.g., primary, secondary,
                                    etc.), or other categorization.
                                 </li>
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/context">context</a></span> The
                                    historical, social, intellectual, artistic, or other context within which the work
                                    was originally conceived (e.g., the 17th century restoration of the monarchy in
                                    England, the aesthetic movement of the late 19th century, etc.) or the historical,
                                    social, intellectual, artistic, or other context within which the expression was
                                    realized.
                                 </li>
                                 
                              </ul>
                              <p>The intended audience for the work and additional information about context for
                                 the work that is not captured in more specific elements elsewhere, such as <a class="link_odd_elementSpec" href="/documentation/2.1.1/history">history</a> and its sub-components, may be recorded in the
                                 <a class="link_odd_elementSpec" href="/documentation/2.1.1/audience">audience</a> and <a class="link_odd_elementSpec" href="/documentation/2.1.1/context">context</a>
                                 elements.
                              </p>
                           </div>
                           <div class="div3" id="workContents">
                              <h3><span class="headingNumber">2.3.9 </span><span class="head">Work Contents</span></h3>
                              <ul class="specList">
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/contents">contents</a></span>
                                    Description of the material contained within a resource.
                                 </li>
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/contentItem">contentItem</a></span>
                                    Contains a single entry within a content description element.
                                 </li>
                                 
                              </ul>
                              <p>Often, it is helpful to identify an entity by listing its constituent parts. A
                                 simple description of the work's content, such as may be found in a bibliographic
                                 record, can be given in single paragraph element:
                              </p>
                              <div id="index.xml-egXML-d39e4517" class="pre egXML_valid">
                                 <span data-indentation="1" class="element">&lt;contents&gt;</span><br />   <span data-indentation="2" class="element">&lt;p&gt;</span>A suitable tone ; Left hand colouring ; Rhythm and accent ; Tempo ; Flexibility ;
                                     Ornaments<span data-indentation="2" class="element">&lt;/p&gt;</span><br />
                                 <span data-indentation="1" class="element">&lt;/contents&gt;</span>
                                 
                              </div>
                              <p>Alternatively, a structured list of contents may be constructed using the <a class="link_odd_elementSpec" href="/documentation/2.1.1/contentItem">contentItem</a> element:
                              </p>
                              <div id="index.xml-egXML-d39e4530" class="pre egXML_valid">
                                 <span data-indentation="1" class="element">&lt;contents&gt;</span><br />   <span data-indentation="2" class="element">&lt;contentItem&gt;</span>Sonata in D major, op. V, no. 1 / Corelli<span data-indentation="2" class="element">&lt;/contentItem&gt;</span><br />   <span data-indentation="2" class="element">&lt;contentItem&gt;</span>Sonata in G minor / Purcell (with Robert Donington, gamba)<span data-indentation="2" class="element">&lt;/contentItem&gt;</span><br />   <span data-indentation="2" class="element">&lt;contentItem&gt;</span>Forlane from Concert royal no. 3 / Couperin<span data-indentation="2" class="element">&lt;/contentItem&gt;</span><br />
                                 <span data-indentation="1" class="element">&lt;/contents&gt;</span>
                                 
                              </div>
                              <p>Each <a class="link_odd_elementSpec" href="/documentation/2.1.1/contentItem">contentItem</a> element may be preceded by an
                                 optional <a class="link_odd_elementSpec" href="/documentation/2.1.1/label">label</a>:
                              </p>
                              <div id="index.xml-egXML-d39e4552" class="pre egXML_valid">
                                 <span data-indentation="1" class="element">&lt;contents&gt;</span><br />   <span data-indentation="2" class="element">&lt;label&gt;</span>1<span data-indentation="2" class="element">&lt;/label&gt;</span><br /><span data-indentation="2" class="element">&lt;contentItem&gt;</span>Sonata in D major, op. V, no. 1 / Corelli<span data-indentation="2" class="element">&lt;/contentItem&gt;</span><br />   <span data-indentation="2" class="element">&lt;label&gt;</span>2<span data-indentation="2" class="element">&lt;/label&gt;</span><br /><span data-indentation="2" class="element">&lt;contentItem&gt;</span>Sonata in G minor / Purcell (with Robert Donington,
                                     gamba)<span data-indentation="2" class="element">&lt;/contentItem&gt;</span><br />   <span data-indentation="2" class="element">&lt;label&gt;</span>3<span data-indentation="2" class="element">&lt;/label&gt;</span><br /><span data-indentation="2" class="element">&lt;contentItem&gt;</span>Forlane from Concert royal no. 3 / Couperin<span data-indentation="2" class="element">&lt;/contentItem&gt;</span><br />
                                 <span data-indentation="1" class="element">&lt;/contents&gt;</span>
                                 
                              </div>
                              <p>To reference a contents list in an external location, use the <span class="att">target</span> attribute:
                              </p>
                              <div id="index.xml-egXML-d39e4577" class="pre egXML_valid">
                                 <span data-indentation="1" class="element">&lt;contents <span class="attribute">target</span>="<span class="attributevalue">http://www.contentProvider.org/toc/toc01.html</span>"/&gt;</span>
                                 
                              </div>
                              <p>To facilitate the creation of music catalogs based on MEI header information,
                                 <a class="link_odd_elementSpec" href="/documentation/2.1.1/contents">contents</a> may contain a heading:
                              </p>
                              <div id="index.xml-egXML-d39e4587" class="pre egXML_valid">
                                 <span data-indentation="1" class="element">&lt;contents&gt;</span><br />   <span data-indentation="2" class="element">&lt;head&gt;</span>Contents of this Work:<span data-indentation="2" class="element">&lt;/head&gt;</span><br />
                                   <span data-indentation="2" class="element">&lt;contentItem&gt;</span>Sonata No. 1<span data-indentation="2" class="element">&lt;/contentItem&gt;</span><br />   <span data-indentation="2" class="element">&lt;contentItem&gt;</span>Sonata No. 2 <span data-indentation="2" class="element">&lt;/contentItem&gt;</span><br />   <span data-indentation="2" class="element">&lt;contentItem&gt;</span>Sonata No. 3<span data-indentation="2" class="element">&lt;/contentItem&gt;</span><br />
                                 <span data-indentation="1" class="element">&lt;/contents&gt;</span>
                                 
                              </div>
                           </div>
                           <div class="teidiv2" id="workBiblList">
                              <h3><span class="headingNumber">2.3.10 </span><span class="head">Bibliographic Evidence</span></h3>
                              <p><span class="li" style="display:list-item"><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/biblList">biblList</a></span> List of bibliographic
                                    references.</span></p>
                              <p>The <a class="link_odd_elementSpec" href="/documentation/2.1.1/biblList">biblList</a> element allows
                                 citation of bibliographic evidence supporting assertions made within other
                                 sub-components of the work description.
                              </p>
                           </div>
                           <div class="div3" id="workNotes">
                              <h3><span class="headingNumber">2.3.11 </span><span class="head">Notes
                                    Statement</span></h3>
                              <p>The <a class="link_odd_elementSpec" href="/documentation/2.1.1/notesStmt">notesStmt</a> element may be
                                 used within the description of the musical work to capture information not accounted
                                 for by the other elements of the description.
                              </p>
                           </div>
                           <div class="div3" id="workClass">
                              <h3><span class="headingNumber">2.3.12 </span><span class="head">Classification</span></h3>
                              <p>The next component of the core <a class="link_odd_elementSpec" href="/documentation/2.1.1/workDesc">workDesc</a> element is the <a class="link_odd_elementSpec" href="/documentation/2.1.1/classification">classification</a> element. This element is used to classify a musical
                                 text according to one or more of the following methods:
                              </p>
                              <ul>
                                 
                                 <li class="item">by reference to a recognized international classification scheme such
                                    as the Dewey Decimal Classification, the Universal Decimal Classification, the Colon
                                    Classification, the Library of Congress Classification, or any other system widely
                                    used in library and documentation work
                                 </li>
                                 
                                 <li class="item">by providing a set of keywords, as provided, for example, by British
                                    Library or Library of Congress Cataloguing in Publication data.
                                 </li>
                                 
                              </ul>
                              <p>The following elements are provided for this purpose:</p>
                              <ul class="specList">
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/termList">termList</a></span>
                                    Collection of text phrases which describe a resource.
                                 </li>
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/classCode">classCode</a></span>
                                    (classification code) – Holds a citation to the source of controlled-vocabulary
                                    terms used in the &lt;termList&gt; element; for example, Library of Congress Subject
                                    Headings (LCSH), Library of Congress Classification (LCC), Library of Congress Name
                                    Authority File (LCNAF), or other thesaurus or ontology.
                                 </li>
                                 
                              </ul>
                              <p>The <a class="link_odd_elementSpec" href="/documentation/2.1.1/termList">termList</a> element categorizes an individual
                                 text by supplying a set of terms which may describe its topic or subject matter, its
                                 physical or intellectual form, date, etc. Each term is indicated by a <a class="link_odd_elementSpec" href="/documentation/2.1.1/term">term</a> element. In some schemes, the order of items in the list is
                                 significant, for example, from major topic to minor; in others, the list has an
                                 organized substructure of its own. No recommendations are made here as to which method
                                 is to be preferred. Wherever possible, such terms should be taken from a recognized
                                 source.
                              </p>
                              <p>The classCode element offers the possibility of capturing a
                                 bibliographic citation and/or a URI at which the classification scheme or information
                                 about it may be found.
                              </p>
                              <div id="index.xml-egXML-d39e4658" class="pre egXML_valid">
                                 <span data-indentation="1" class="element">&lt;classCode <span class="attribute">xml:id</span>="<span class="attributevalue">header.LoC_lccoA</span>"&gt;</span>Library of Congress subject headings. Prepared by the
                                   Cataloging Policy and Support Office, Collections Services. Washington, D.C.: Library of
                                   Congress, Cataloging Distribution Service, 1993- .<span data-indentation="1" class="element">&lt;/classCode&gt;</span>
                                 
                              </div>
                              <div id="index.xml-egXML-d39e4663" class="pre egXML_valid">
                                 <span data-indentation="1" class="element">&lt;classCode <span class="attribute">authURI</span>="<span class="attributevalue">http://www.loc.gov/aba/cataloging/classification/lcco/lcco_m.pdf</span>" <span class="attribute">xml:id</span>="<span class="attributevalue">header.LoC_lccoB</span>"/&gt;</span>
                                 
                              </div>
                              <div id="index.xml-egXML-d39e4667" class="pre egXML_valid">
                                 <span data-indentation="1" class="element">&lt;classCode <span class="attribute">authURI</span>="<span class="attributevalue">http://www.loc.gov/aba/cataloging/classification/lcco/lcco_m.pdf</span>" <span class="attribute">xml:id</span>="<span class="attributevalue">header.LoC_lccoC</span>"&gt;</span>Library of
                                   Congress subject headings. Prepared by the Cataloging Policy and Support Office,
                                   Collections Services. Washington, D.C.: Library of Congress, Cataloging Distribution
                                   Service, 1993- .<span data-indentation="1" class="element">&lt;/classCode&gt;</span>
                                 
                              </div>
                              <p>The <span class="att">classcode</span> attribute may be used on each term
                                 element to make reference, by means of an identifier, to the classification scheme
                                 from which it is drawn.
                              </p>
                              <div id="index.xml-egXML-d39e4678" class="pre egXML_valid">
                                 <span data-indentation="1" class="element">&lt;classification&gt;</span><br />   <span data-indentation="2" class="element">&lt;classCode <span class="attribute">authURI</span>="<span class="attributevalue">http://www.loc.gov</span>" <span class="attribute">authority</span>="<span class="attributevalue">Library of Congress</span>" <span class="attribute">xml:id</span>="<span class="attributevalue">header.LCSH1</span>"/&gt;</span><br />   <span data-indentation="2" class="element">&lt;classCode <span class="attribute">authURI</span>="<span class="attributevalue">http://www.loc.gov/aba/cataloging/classification/lcco/lcco_m.pdf</span>" <span class="attribute">authority</span>="<span class="attributevalue">Library of
                                       Congress</span>" <span class="attribute">xml:id</span>="<span class="attributevalue">header.LoC_lcco1</span>"/&gt;</span><br />   <span data-indentation="2" class="element">&lt;termList&gt;</span><br />     <span data-indentation="3" class="element">&lt;term <span class="attribute">classcode</span>="<span class="attributevalue">#header.LCSH1</span>"&gt;</span>Guitar music (Rock)<span data-indentation="3" class="element">&lt;/term&gt;</span><br />     <span data-indentation="3" class="element">&lt;term <span class="attribute">classcode</span>="<span class="attributevalue">#header.LCSH1</span>"&gt;</span>Rock music 1971-1980.<span data-indentation="3" class="element">&lt;/term&gt;</span><br />     <span data-indentation="3" class="element">&lt;term <span class="attribute">classcode</span>="<span class="attributevalue">#header.LoC_lcco1</span>"&gt;</span>M1630.18.Z26 O6 2011<span data-indentation="3" class="element">&lt;/term&gt;</span><br />   <span data-indentation="2" class="element">&lt;/termList&gt;</span><br />
                                 <span data-indentation="1" class="element">&lt;/classification&gt;</span>
                                 
                              </div>
                              <p>Alternatively, <span class="att">classcode</span> may be used on <a class="link_odd_elementSpec" href="/documentation/2.1.1/termList">termList</a> when all the contained terms come from the same
                                 source.
                              </p>
                              <div id="index.xml-egXML-d39e4707" class="pre egXML_valid">
                                 <span data-indentation="1" class="element">&lt;classification&gt;</span><br />   <span data-indentation="2" class="element">&lt;classCode <span class="attribute">authURI</span>="<span class="attributevalue">http://www.loc.gov</span>" <span class="attribute">authority</span>="<span class="attributevalue">Library of Congress</span>" <span class="attribute">xml:id</span>="<span class="attributevalue">header.LCSH2</span>"/&gt;</span><br />   <span data-indentation="2" class="element">&lt;classCode <span class="attribute">authURI</span>="<span class="attributevalue">http://www.loc.gov/aba/cataloging/classification/lcco/lcco_m.pdf</span>" <span class="attribute">authority</span>="<span class="attributevalue">Library of
                                       Congress</span>" <span class="attribute">xml:id</span>="<span class="attributevalue">header.LoC_lcco2</span>"/&gt;</span><br />   <span data-indentation="2" class="element">&lt;termList <span class="attribute">classcode</span>="<span class="attributevalue">#header.LCSH2</span>"&gt;</span><br />     <span data-indentation="3" class="element">&lt;term&gt;</span>Guitar music (Rock) <span data-indentation="3" class="element">&lt;/term&gt;</span><br />
                                     <span data-indentation="3" class="element">&lt;term&gt;</span>Rock music 1971-1980.<span data-indentation="3" class="element">&lt;/term&gt;</span><br />   <span data-indentation="2" class="element">&lt;/termList&gt;</span><br />   <span data-indentation="2" class="element">&lt;termList <span class="attribute">classcode</span>="<span class="attributevalue">#header.LoC_lcco2</span>"&gt;</span><br />     <span data-indentation="3" class="element">&lt;term&gt;</span>M1630.18.Z26 O6 2011<span data-indentation="3" class="element">&lt;/term&gt;</span><br />
                                   <span data-indentation="2" class="element">&lt;/termList&gt;</span><br />
                                 <span data-indentation="1" class="element">&lt;/classification&gt;</span>
                                 
                              </div>
                           </div>
                           <div class="div3" id="workRelationships">
                              <h3><span class="headingNumber">2.3.13 </span><span class="head">Work Relationships</span></h3>
                              <p>When the FRBR
                                 (Functional Requirements for Bibliographic Records) module is available, the following
                                 elements may be used within <a class="link_odd_elementSpec" href="/documentation/2.1.1/work">work</a> to describe
                                 relationships between the work being described and other works or between the work
                                 and
                                 expressions of it:
                              </p>
                              <ul class="specList">
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/expressionList">expressionList</a></span> Gathers bibliographic expression entities.
                                 </li>
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/componentGrp">componentGrp</a></span>
                                    (component group) – The child elements of this element are treated as parts of the
                                    elements header. Although this is an implicit way of expressing FRBR's hasPart /
                                    isPartOf -relationships, it avoids this terminology in order to prevent confusion
                                    with musical terminology. All children of a component must be the same type as its
                                    parent: works within work, items in item, etc.
                                 </li>
                                 
                                 <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/relationList">relationList</a></span>
                                    Gathers bibliographic relation elements.
                                 </li>
                                 
                              </ul>
                              <p>For more information about FRBR and the use of these elements, see chapter <a class="link_ptr" href="/documentation/2.1.1/FRBR" title="1"><span class="headingNumber">3
                                       </span>Functional Requirements for Bibliographic Records
                                    (FRBR)</a>.
                              </p>
                           </div>
                        </div>
                        <div class="div2" id="revisionDescription">
                           <h2><span class="headingNumber">2.4 </span><span class="head">Revision
                                 Description</span></h2>
                           <p>The final sub-element of the MEI header, the <a class="link_odd_elementSpec" href="/documentation/2.1.1/revisionDesc">revisionDesc</a> element, provides a detailed change log in which each
                              change made to a text may be recorded. Its use is optional but highly recommended.
                              It
                              provides essential information for the administration of large numbers of files which
                              are being updated, corrected, or otherwise modified as well as extremely useful
                              documentation for files being passed from researcher to researcher or system to system.
                              Without change logs, it is easy to confuse different versions of a file, or to remain
                              unaware of small but important changes made in the file by some earlier link in the
                              chain of distribution. No change should be made in any MEI-conformant file without
                              corresponding entries being made in the change log.
                           </p>
                           <ul class="specList">
                              
                              <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/revisionDesc">revisionDesc</a></span>
                                 (revision description) – Container for information about alterations that have been
                                 made to an MEI file.
                              </li>
                              
                              <li><span class="specList-elementSpec"><a class="link_odd_elementSpec" href="/documentation/2.1.1/change">change</a></span> Individual
                                 change within the revision description.
                              </li>
                              
                           </ul>
                           <p>The main purpose of the revision description is to record changes in the text to
                              which a header is prefixed. However, it is recommended practice to include entries
                              also
                              for significant changes in the header itself (other than the revision description
                              itself, of course). At the very least, an entry should be supplied indicating the
                              date
                              of creation of the header.
                           </p>
                           <p>The log consists of a list of <a class="link_odd_elementSpec" href="/documentation/2.1.1/change">change</a> elements, each of which contains a detailed description of the
                              changes made. If a number is to be associated with one or more changes (for example,
                              a
                              revision number), the <span class="att">n</span> attribute may be used to indicate it.
                              The person responsible for the change and the date of the change may be indicated
                              by the
                              <a class="link_odd_elementSpec" href="/documentation/2.1.1/respStmt">respStmt</a> and <a class="link_odd_elementSpec" href="/documentation/2.1.1/date">date</a>
                              elements. The description of the change itself is contained within the <a class="link_odd_elementSpec" href="/documentation/2.1.1/changeDesc">changeDesc</a> element, which can hold one or more paragraphs.
                           </p>
                           <p>It is
                              recommended to give changes in reverse chronological order, most recent first.
                           </p>
                           <p>For
                              example:
                           </p>
                           <div id="index.xml-egXML-d39e4787" class="pre egXML_valid">
                              <span data-indentation="1" class="element">&lt;revisionDesc&gt;</span><br />   <span data-indentation="2" class="element">&lt;change <span class="attribute">n</span>="<span class="attributevalue">4</span>"&gt;</span><br />     <span data-indentation="3" class="element">&lt;respStmt&gt;</span><br />       <span data-indentation="4" class="element">&lt;persName&gt;</span>KR<span data-indentation="4" class="element">&lt;/persName&gt;</span><br />     <span data-indentation="3" class="element">&lt;/respStmt&gt;</span><br />     <span data-indentation="3" class="element">&lt;changeDesc&gt;</span><br />       <span data-indentation="4" class="element">&lt;p&gt;</span>Cleaned up MEI file automatically using Header.xsl.<span data-indentation="4" class="element">&lt;/p&gt;</span><br />     <span data-indentation="3" class="element">&lt;/changeDesc&gt;</span><br />
                                  <span data-indentation="3" class="element">&lt;date <span class="attribute">isodate</span>="<span class="attributevalue">2011-12-01</span>"/&gt;</span><br />   <span data-indentation="2" class="element">&lt;/change&gt;</span><br />   <span data-indentation="2" class="element">&lt;change <span class="attribute">n</span>="<span class="attributevalue">3</span>"&gt;</span><br />     <span data-indentation="3" class="element">&lt;respStmt&gt;</span><br />       <span data-indentation="4" class="element">&lt;persName&gt;</span>KR<span data-indentation="4" class="element">&lt;/persName&gt;</span><br />     <span data-indentation="3" class="element">&lt;/respStmt&gt;</span><br />     <span data-indentation="3" class="element">&lt;changeDesc&gt;</span><br />       <span data-indentation="4" class="element">&lt;p&gt;</span>Cleaned up MEI file automatically using ppq.xsl.<span data-indentation="4" class="element">&lt;/p&gt;</span><br />     <span data-indentation="3" class="element">&lt;/changeDesc&gt;</span><br />     <span data-indentation="3" class="element">&lt;date <span class="attribute">isodate</span>="<span class="attributevalue">2011-10-21</span>"/&gt;</span><br />   <span data-indentation="2" class="element">&lt;/change&gt;</span><br />
                              <span data-indentation="1" class="element">&lt;/revisionDesc&gt;</span>
                              
                           </div>
                           <p>A slightly shorter form for recording changes is also available when a the date
                              of the change can be described by a single date in a standard ISO form and when the
                              name
                              of the agent(s) responsible for the change, encoded elsewhere in the header, can be
                              referred to by one or more URIs given in the <span class="att">resp</span> attribute.
                              For example:
                           </p>
                           <div id="index.xml-egXML-d39e4831" class="pre egXML_valid">
                              <span data-indentation="1" class="element">&lt;change <span class="attribute">isodate</span>="<span class="attributevalue">2011-10-21</span>" <span class="attribute">n</span>="<span class="attributevalue">3</span>" <span class="attribute">resp</span>="<span class="attributevalue">#KR #MH</span>"&gt;</span><br />   <span data-indentation="2" class="element">&lt;changeDesc&gt;</span><br />     <span data-indentation="3" class="element">&lt;p&gt;</span>Cleaned up MEI file automatically using ppq.xsl.<span data-indentation="3" class="element">&lt;/p&gt;</span><br />   <span data-indentation="2" class="element">&lt;/changeDesc&gt;</span><br />
                              <span data-indentation="1" class="element">&lt;/change&gt;</span>     
                           </div>
                        </div>
                        <div class="div2" id="minimalRecommendedHeader">
                           <h2><span class="headingNumber">2.5 </span><span class="head">Minimal and Recommended Header Information</span></h2>
                           <p>The MEI header
                              allows for the provision of a very large amount of information concerning the text
                              itself, its source, its encodings, and revisions of it, as well as a wealth of
                              descriptive information, such as the languages it uses and the situation(s) in which
                              it
                              was produced, together with the setting and identity of participants within it. This
                              diversity and richness reflects the diversity of uses to which it is envisaged that
                              electronic texts conforming to these Guidelines will be put. It is emphatically not
                              intended that all of the elements described above should be present in every MEI
                              Header.
                           </p>
                           <p>The amount of encoding in a header will depend both on the nature and the
                              intended use of the text. At one extreme, an encoder may expect that the header will
                              be
                              needed only to provide a bibliographic identification of the text adequate to local
                              needs. At the other, wishing to ensure that their texts can be used for the widest
                              range
                              of applications, encoders will want to document as explicitly as possible both
                              bibliographic and descriptive information, in such a way that no prior or ancillary
                              knowledge about the text is needed in order to process it. The header in such a case
                              will be very full, approximating the kind of documentation often supplied in the form
                              of
                              a manual. Most texts will lie somewhere between these extremes; textual corpora in
                              particular will tend more to the latter extreme. In the remainder of this section
                              we
                              demonstrate first the minimal, and then a commonly recommended, level of encoding
                              for
                              the bibliographic information held by the MEI header.
                           </p>
                           <p>Supplying only the level of
                              encoding required, the MEI header of a single text will look like the following
                              example:
                           </p>
                           <div id="index.xml-egXML-d39e4851" class="pre egXML_valid">
                              <span data-indentation="1" class="element">&lt;meiHead&gt;</span><br />   <span data-indentation="2" class="element">&lt;fileDesc&gt;</span><br />     <span data-indentation="3" class="element">&lt;titleStmt&gt;</span><br />
                                    <span data-indentation="4" class="element">&lt;title&gt;</span>Fughette (in Gottes Namen Fahren wir - Dies sind die heil'gen zehn Gebote) for
                                      Brass Quintett : an electronic transcription<span data-indentation="4" class="element">&lt;/title&gt;</span><br />     <span data-indentation="3" class="element">&lt;/titleStmt&gt;</span><br />     <span data-indentation="3" class="element">&lt;pubStmt&gt;</span><br />       <span data-indentation="4" class="element">&lt;respStmt&gt;</span><br />         <span data-indentation="5" class="element">&lt;corpName <span class="attribute">authURI</span>="<span class="attributevalue">http://d-nb.info/gnd</span>" <span class="attribute">authority</span>="<span class="attributevalue">GND</span>" <span class="attribute">dbkey</span>="<span class="attributevalue">5115204-6</span>"&gt;</span>Musikwissenschaftliches Seminar &lt;Detmold&gt;<span data-indentation="5" class="element">&lt;/corpName&gt;</span><br />       <span data-indentation="4" class="element">&lt;/respStmt&gt;</span><br />     <span data-indentation="3" class="element">&lt;/pubStmt&gt;</span><br />   <span data-indentation="2" class="element">&lt;/fileDesc&gt;</span><br />
                              <span data-indentation="1" class="element">&lt;/meiHead&gt;</span>
                              
                           </div>
                           <p>The only mandatory component of the MEI Header is the <a class="link_odd_elementSpec" href="/documentation/2.1.1/fileDesc">fileDesc</a> element. Within this element, <a class="link_odd_elementSpec" href="/documentation/2.1.1/titleStmt">titleStmt</a> and <a class="link_odd_elementSpec" href="/documentation/2.1.1/pubStmt">pubStmt</a> are required
                              constituents. Within the title statement, a title is required. Within the <a class="link_odd_elementSpec" href="/documentation/2.1.1/pubStmt">pubStmt</a>, a publisher, distributor, or other agency
                              responsible for the file is required.
                           </p>
                           <p>While not formally required, additional
                              information is recommended for a minimally effective header. For example, it is
                              recommended that the person or corporate entity responsible for the creation of the
                              encoding should be specified using <a class="link_odd_elementSpec" href="/documentation/2.1.1/respStmt">respStmt</a> within the
                              <a class="link_odd_elementSpec" href="/documentation/2.1.1/titleStmt">titleStmt</a> element. It is also recommended that
                              information about the source, or sources, of the encoding be included. Each <a class="link_odd_elementSpec" href="/documentation/2.1.1/source">source</a> element should contain at the least a loosely
                              structured bibliographic citation that identifies the source used to construct the
                              MEI
                              file.
                           </p>
                           <p>Furthermore, If the electronic transcription is a member of a series of
                              publications, the series title and publisher should be included using the <a class="link_odd_elementSpec" href="/documentation/2.1.1/seriesStmt">seriesStmt</a> element. It is also common for cataloging records
                              to include genre and/or form information, here represented by the MEI <a class="link_odd_elementSpec" href="/documentation/2.1.1/classification">classification</a> element.
                           </p>
                           <p>We now present the same example header,
                              expanded to include additionally recommended information, adequate for most
                              bibliographic purposes, in particular to allow for the creation of an AACR2-conformant
                              bibliographic record.
                           </p>
                           <div id="index.xml-egXML-d39e4909" class="pre egXML_valid">
                              <span data-indentation="1" class="element">&lt;meiHead&gt;</span><br />   <span data-indentation="2" class="element">&lt;fileDesc&gt;</span><br />     <span data-indentation="3" class="element">&lt;titleStmt&gt;</span><br />
                                    <span data-indentation="4" class="element">&lt;title&gt;</span>Fughette (in Gottes Namen Fahren wir - Dies sind die heil'gen zehn Gebote) for
                                      Brass Quintett : an electronic transcription<span data-indentation="4" class="element">&lt;/title&gt;</span><br />       <span data-indentation="4" class="element">&lt;respStmt&gt;</span><br />
                                      <span data-indentation="5" class="element">&lt;resp&gt;</span>Encoded by:<span data-indentation="5" class="element">&lt;/resp&gt;</span><br />         <span data-indentation="5" class="element">&lt;persName <span class="attribute">xml:id</span>="<span class="attributevalue">header.MH</span>"&gt;</span>Maja Hartwig<span data-indentation="5" class="element">&lt;/persName&gt;</span><br />         <span data-indentation="5" class="element">&lt;persName <span class="attribute">xml:id</span>="<span class="attributevalue">header.KR</span>"&gt;</span>Kristina Richts<span data-indentation="5" class="element">&lt;/persName&gt;</span><br />       <span data-indentation="4" class="element">&lt;/respStmt&gt;</span><br />
                                  <span data-indentation="3" class="element">&lt;/titleStmt&gt;</span><br />     <span data-indentation="3" class="element">&lt;pubStmt&gt;</span><br />       <span data-indentation="4" class="element">&lt;respStmt&gt;</span><br />
                                      <span data-indentation="5" class="element">&lt;corpName&gt;</span>Musikwissenschaftliches Seminar &lt;Detmold&gt;<span data-indentation="5" class="element">&lt;/corpName&gt;</span><br />       <span data-indentation="4" class="element">&lt;/respStmt&gt;</span><br />       <span data-indentation="4" class="element">&lt;date&gt;</span>2011<span data-indentation="4" class="element">&lt;/date&gt;</span><br />     <span data-indentation="3" class="element">&lt;/pubStmt&gt;</span><br />
                                  <span data-indentation="3" class="element">&lt;seriesStmt&gt;</span><br />       <span data-indentation="4" class="element">&lt;title&gt;</span>MEI Sample Collection<span data-indentation="4" class="element">&lt;/title&gt;</span><br />
                                    <span data-indentation="4" class="element">&lt;respStmt&gt;</span><br />         <span data-indentation="5" class="element">&lt;corpName <span class="attribute">role</span>="<span class="attributevalue">publisher</span>"&gt;</span>MEI Project<span data-indentation="5" class="element">&lt;/corpName&gt;</span><br />       <span data-indentation="4" class="element">&lt;/respStmt&gt;</span><br />
                                  <span data-indentation="3" class="element">&lt;/seriesStmt&gt;</span><br />     <span data-indentation="3" class="element">&lt;sourceDesc&gt;</span><br />       <span data-indentation="4" class="element">&lt;source&gt;</span><br />
                                      <span data-indentation="5" class="element">&lt;titleStmt&gt;</span><br />           <span data-indentation="6" class="element">&lt;title&gt;</span>Fughette (in Gottes Namen Fahren wir - Dies sind die heil'gen zehn Gebote)
                                          for Brass Quintett<span data-indentation="6" class="element">&lt;/title&gt;</span><br />
                                        <span data-indentation="6" class="element">&lt;respStmt&gt;</span><br />             <span data-indentation="7" class="element">&lt;persName <span class="attribute">role</span>="<span class="attributevalue">composer</span>"&gt;</span>Johann Christoph Bach<span data-indentation="7" class="element">&lt;/persName&gt;</span><br />             <span data-indentation="7" class="element">&lt;persName <span class="attribute">role</span>="<span class="attributevalue">arranger</span>"&gt;</span>Michel Rondeau<span data-indentation="7" class="element">&lt;/persName&gt;</span><br />           <span data-indentation="6" class="element">&lt;/respStmt&gt;</span><br />
                                      <span data-indentation="5" class="element">&lt;/titleStmt&gt;</span><br />         <span data-indentation="5" class="element">&lt;pubStmt&gt;</span><br />           <span data-indentation="6" class="element">&lt;identifier <span class="attribute">type</span>="<span class="attributevalue">URI</span>"&gt;</span>http://icking-music-archive.org/scores/j.chr.bach/JCBIN-xml.zip<span data-indentation="6" class="element">&lt;/identifier&gt;</span><br />           <span data-indentation="6" class="element">&lt;date <span class="attribute">isodate</span>="<span class="attributevalue">2011-10-13</span>"/&gt;</span><br />           <span data-indentation="6" class="element">&lt;respStmt&gt;</span><br />             <span data-indentation="7" class="element">&lt;name&gt;</span>Werner Icking Music Archive<span data-indentation="7" class="element">&lt;/name&gt;</span><br />           <span data-indentation="6" class="element">&lt;/respStmt&gt;</span><br />
                                        <span data-indentation="6" class="element">&lt;availability&gt;</span><br />             <span data-indentation="7" class="element">&lt;useRestrict&gt;</span>© 2010 - Gatineau,Qc.Ca.<span data-indentation="7" class="element">&lt;/useRestrict&gt;</span><br />           <span data-indentation="6" class="element">&lt;/availability&gt;</span><br />         <span data-indentation="5" class="element">&lt;/pubStmt&gt;</span><br />
                                      <span data-indentation="5" class="element">&lt;classification&gt;</span><br />           <span data-indentation="6" class="element">&lt;classCode <span class="attribute">authURI</span>="<span class="attributevalue">http://www.oclc.org/dewey/resources/summaries/default.htm#700</span>" <span class="attribute">authority</span>="<span class="attributevalue">OCLC</span>" <span class="attribute">xml:id</span>="<span class="attributevalue">header.OCLC_DDC</span>"/&gt;</span><br />           <span data-indentation="6" class="element">&lt;termList&gt;</span><br />             <span data-indentation="7" class="element">&lt;term <span class="attribute">classcode</span>="<span class="attributevalue">#header.OCLC_DDC</span>"&gt;</span>785.15<span data-indentation="7" class="element">&lt;/term&gt;</span><br />
                                        <span data-indentation="6" class="element">&lt;/termList&gt;</span><br />         <span data-indentation="5" class="element">&lt;/classification&gt;</span><br />       <span data-indentation="4" class="element">&lt;/source&gt;</span><br />
                                  <span data-indentation="3" class="element">&lt;/sourceDesc&gt;</span><br />   <span data-indentation="2" class="element">&lt;/fileDesc&gt;</span><br />
                              <span data-indentation="1" class="element">&lt;/meiHead&gt;</span>
                              
                           </div>
                        </div>
                        <div class="div2" id="independentHeader">
                           <h2><span class="headingNumber">2.6
                                 </span><span class="head">Independent Headers</span></h2>
                           <p>Many libraries,
                              repositories, research sites and related institutions collect bibliographic and
                              documentary information about machine readable music documents without necessarily
                              collecting the music documents themselves. Such institutions may thus want access
                              to the
                              header of an MEI document without its attached text in order to build catalogs, indexes
                              and databases that can be used to locate relevant texts at remote locations, obtain
                              full
                              documentation about those texts, and learn how to obtain them. This section describes
                              a
                              set of practices by which the metadata headers of MEI documents can be encoded
                              separately from those documents and exchanged as freestanding MEI documents. Headers
                              exchanged independently of the documents they describe are called independent
                              headers.
                           </p>
                           <div class="div3" id="independentHeaderDefinition">
                              <h3><span class="headingNumber">2.6.1 </span><span class="head">Definition and Principles for
                                    Encoders</span></h3>
                              <p>An independent header is an MEI metadata header that can be
                                 exchanged as an independent document between libraries, archives, collections,
                                 projects, and individuals.
                              </p>
                              <p>The structure of an independent header is exactly the
                                 same as that of an header attached to a document. This means that an <a class="link_odd_elementSpec" href="/documentation/2.1.1/meiHead">meiHead</a> can be extracted from an MEI document and sent to a
                                 receiving institution with little or no change.
                              </p>
                              <p>When deciding which information
                                 to include in the independent header, and the format or structure of that information,
                                 the following should be kept in mind:
                              </p>
                              <ul>
                                 
                                 <li class="item">The independent header should provide full bibliographic information
                                    about the encoded text, its sources, where the text can be located, and any
                                    restrictions governing its use.
                                 </li>
                                 
                                 <li class="item">The independent header should contain useful information about the
                                    encoding of the text itself. In this regard, it is highly recommended that the
                                    encoding description be as complete as possible. The Guidelines do not require that
                                    the encoding description be included in the header (since some simple transcriptions
                                    of small items may not require it), but in practice the use of a header without an
                                    encoding description would be severely limited.
                                 </li>
                                 
                                 <li class="item">The independent header should be amenable to automatic processing,
                                    particularly for loading into databases and for the creation of publications,
                                    indexes, and finding aids, without undue editorial intervention on the part of the
                                    receiving institution. For this reason, two recommendations are made regarding the
                                    format or structure of the header: first, where there is a choice between a prose
                                    content model and one that contains a formal series of specialized elements,
                                    wherever possible and appropriate the specialized elements should be preferred to
                                    unstructured prose. Second, with respect to corpora, information about each of the
                                    texts within a corpus should be included in the overall corpus-level <a class="link_odd_elementSpec" href="/documentation/2.1.1/meiHead">meiHead</a>. That is, source information, editorial
                                    practices, encoding descriptions, and the like should be included in the relevant
                                    sections of the corpus <a class="link_odd_elementSpec" href="/documentation/2.1.1/meiHead">meiHead</a>, with pointers to
                                    them from the headers of the individual texts included in the corpus. There are
                                    three reasons for this recommendation: first, the corpus-level header will contain
                                    the full array of bibliographic and documentary information for each of the texts
                                    in
                                    a corpus, and thus be of great benefit to remote users, who may have access only to
                                    the independent header; second, such a layout is easier for the coder to maintain
                                    than searching for information throughout a text; and third, generally speaking,
                                    this practice results in greater overall consistency, especially with respect to
                                    bibliographic citations.
                                 </li>
                                 
                              </ul>
                           </div>
                           <div class="div3" id="biblAnalog">
                              <h3><span class="headingNumber">2.6.2
                                    </span><span class="head">Header Elements and their Relationship to Other
                                    Bibliographic Standards</span></h3>
                              <p>Mapping elements from the MEI metadata header
                                 to another descriptive system may help a repository harvest selected data from the
                                 MEI
                                 file to build a basic catalog record. For this purpose, the following attribute is
                                 provided on most meiHead elements:
                              </p>
                              <ul class="specList">
                                 
                                 <li><span class="specList-classSpec"><a href="/documentation/2.1.1/att.bibl">att.bibl</a></span>
                                    Bibliographic attributes.
                                    <table class="specDesc">
                                       
                                       <tr>
                                          
                                          <td class="Attribute"><span class="att">analog</span></td>
                                          
                                          <td>contains a reference to a field or element in another descriptive encoding
                                             system to which this MEI element is comparable.
                                          </td>
                                          
                                       </tr>
                                       
                                    </table>
                                 </li>
                                 
                              </ul>
                              <p>The encoding system to which fields are mapped must be specified in <span class="att">analog</span>. When possible, subfields as well as fields should be
                                 specified, e.g., subfields within MARC fields.
                              </p>
                           </div>
                        </div>
                        <div class="div2" id="relatedItemVsFRBR">
                           <h2><span class="headingNumber">2.7 </span><span class="head">RelatedItem vs. FRBR</span></h2>
                           <p>MEI offers two related concepts for capturing
                              relations between bibliographic items. The model of <a class="link_odd_elementSpec" href="/documentation/2.1.1/relatedItem">relatedItem</a>, as described in chapter <a class="link_ptr" href="/documentation/2.1.1/shared#relatedItemDesc" title="Related Items"><span class="headingNumber">1.3.7
                                    </span>Related Items</a> of these Guidelines, is derived from MODS v3.4 (see
                              documentation <a class="link_ref" href="http://www.loc.gov/standards/mods/v3/mods-userguide-elements.html#relateditem">here</a>). Its purpose in MEI is to encode bibliographic references between mostly
                              "secondary" material, like reviews, articles, and so on. It may be used to provide
                              cross-references between information encoded in different places of the
                              header.
                           </p>
                           <p>However, <a class="link_odd_elementSpec" href="/documentation/2.1.1/relatedItem">relatedItem</a> is less ideal for
                              describing the relations between works, differing versions of these works, the sources
                              in which those versions are transmitted, and where applicable the individual copies
                              of a
                              print. For these situations, it is strongly recommended to use the <a class="link_ref" href="/documentation/2.1.1/FRBR" title="1">FRBR module</a> instead. This module is based on the Functional
                              Requirements for Bibliographic Records, as <a class="link_ref" href="http://www.ifla.org/publications/functional-requirements-for-bibliographic-records">specified</a> by the <a class="link_ref" href="http://www.ifla.org">IFLA</a>. It
                              allows a much finer description of relationships between such "primary" entities.
                              For
                              compatibility reasons, both models should not be confused or mixed under any
                              circumstances.
                           </p>
                        </div>
                     </section>
                  </div>
               </div>
            </div>
            <div class="panel-grid-cell" style="width: 35%; float: left;">
               <div class="panel widget widget_text panel-first-child panel-last-child">
                  <header class="entry-header">
                     <h1 class="entry-title">
                        MEI Guidelines <small>Version 2.1.1</small></h1>
                  </header>
                  <div class="textwidget">
                     <ul class="guidelinesList">
                        <li><a class="guidelines_mainLink" href="/documentation/2.1.1/chapters">MEI Guidelines</a></li>
                        <li><a class="guidelines_mainLink" href="/documentation/2.1.1/elements">Elements</a></li>
                        <li><a class="guidelines_mainLink" href="/documentation/2.1.1/atts">Attributes</a></li>
                        <li><a class="guidelines_mainLink" href="/documentation/2.1.1/models">Model Classes</a></li>
                        <li><a class="guidelines_mainLink" href="/documentation/2.1.1/data">Data Types</a></li>
                     </ul>
                  </div>
                  <div style="margin: 10px 30px; border-bottom: 0.5px solid #666666; height: 1px;"></div>
                  <h3 class="widget-title">Table of Contents</h3>
                  <div class="textwidget">
                     <ul class="guidelinesList">
                        <li><a href="/documentation/2.1.1/header#"><span class="headingNumber">2 </span><span class="head">The MEI
                                 Header</span></a></li>
                        <li><a href="/documentation/2.1.1/header#fileDescription"><span class="headingNumber">2.1 </span><span class="head">File Description</span></a></li>
                        <li><a href="/documentation/2.1.1/header#titlestmt"><span class="headingNumber">2.1.1 </span><span class="head">Title Statement</span></a></li>
                        <li><a href="/documentation/2.1.1/header#editionstmt"><span class="headingNumber">2.1.2
                                 </span><span class="head">Edition Statement</span></a></li>
                        <li><a href="/documentation/2.1.1/header#physicalDescription"><span class="headingNumber">2.1.3 </span><span class="head">Physical Description of the File</span></a></li>
                        <li><a href="/documentation/2.1.1/header#publicationDistribution"><span class="headingNumber">2.1.4 </span><span class="head">Publication, Distribution,
                                 etc.</span></a></li>
                        <li><a href="/documentation/2.1.1/header#seriesStatement"><span class="headingNumber">2.1.5
                                 </span><span class="head">Series Statement</span></a></li>
                        <li><a href="/documentation/2.1.1/header#notesStatement"><span class="headingNumber">2.1.6 </span><span class="head">Notes Statement</span></a></li>
                        <li><a href="/documentation/2.1.1/header#sourceDescription"><span class="headingNumber">2.1.7 </span><span class="head">Source Description</span></a></li>
                        <li><a href="/documentation/2.1.1/header#associatingMetadataAndData"><span class="headingNumber">2.1.7.1 </span><span class="head">Associating Metadata and Data</span></a></li>
                        <li><a href="/documentation/2.1.1/header#encodingDescription"><span class="headingNumber">2.2 </span><span class="head">Encoding
                                 Description</span></a></li>
                        <li><a href="/documentation/2.1.1/header#applicationInformation"><span class="headingNumber">2.2.1 </span><span class="head">Application Information</span></a></li>
                        <li><a href="/documentation/2.1.1/header#EditorialPrinciples"><span class="headingNumber">2.2.2 </span><span class="head">Declaration of Editorial
                                 Principles</span></a></li>
                        <li><a href="/documentation/2.1.1/header#projectDescription"><span class="headingNumber">2.2.3 </span><span class="head">Project
                                 Description</span></a></li>
                        <li><a href="/documentation/2.1.1/header#samplingDeclaration"><span class="headingNumber">2.2.4 </span><span class="head">Sampling Declaration</span></a></li>
                        <li><a href="/documentation/2.1.1/header#workDescription"><span class="headingNumber">2.3 </span><span class="head">Work
                                 Description</span></a></li>
                        <li><a href="/documentation/2.1.1/header#workIdentification"><span class="headingNumber">2.3.1
                                 </span><span class="head">Work Identification</span></a></li>
                        <li><a href="/documentation/2.1.1/header#workIncipit"><span class="headingNumber">2.3.2 </span><span class="head">Incipits</span></a></li>
                        <li><a href="/documentation/2.1.1/header#workKeyTempoMeter"><span class="headingNumber">2.3.3 </span><span class="head">Key, Tempo, and Meter</span></a></li>
                        <li><a href="/documentation/2.1.1/header#workOtherChar"><span class="headingNumber">2.3.4 </span><span class="head">Other
                                 Identifying Characteristics</span></a></li>
                        <li><a href="/documentation/2.1.1/header#workHistory"><span class="headingNumber">2.3.5 </span><span class="head">Work History</span></a></li>
                        <li><a href="/documentation/2.1.1/header#workLanguage"><span class="headingNumber">2.3.6 </span><span class="head">Language
                                 Usage</span></a></li>
                        <li><a href="/documentation/2.1.1/header#workMedium"><span class="headingNumber">2.3.7
                                 </span><span class="head">Performance Medium</span></a></li>
                        <li><a href="/documentation/2.1.1/header#workCast"><span class="headingNumber">2.3.7.1 </span><span class="head">Cast Lists</span></a></li>
                        <li><a href="/documentation/2.1.1/header#workInstrumentation"><span class="headingNumber">2.3.7.2 </span><span class="head">Instrumentation</span></a></li>
                        <li><a href="/documentation/2.1.1/header#workAudience"><span class="headingNumber">2.3.8 </span><span class="head">Audience and
                                 Context</span></a></li>
                        <li><a href="/documentation/2.1.1/header#workContents"><span class="headingNumber">2.3.9 </span><span class="head">Work Contents</span></a></li>
                        <li><a href="/documentation/2.1.1/header#workBiblList"><span class="headingNumber">2.3.10 </span><span class="head">Bibliographic Evidence</span></a></li>
                        <li><a href="/documentation/2.1.1/header#workNotes"><span class="headingNumber">2.3.11 </span><span class="head">Notes
                                 Statement</span></a></li>
                        <li><a href="/documentation/2.1.1/header#workClass"><span class="headingNumber">2.3.12 </span><span class="head">Classification</span></a></li>
                        <li><a href="/documentation/2.1.1/header#workRelationships"><span class="headingNumber">2.3.13 </span><span class="head">Work Relationships</span></a></li>
                        <li><a href="/documentation/2.1.1/header#revisionDescription"><span class="headingNumber">2.4 </span><span class="head">Revision
                                 Description</span></a></li>
                        <li><a href="/documentation/2.1.1/header#minimalRecommendedHeader"><span class="headingNumber">2.5 </span><span class="head">Minimal and Recommended Header Information</span></a></li>
                        <li><a href="/documentation/2.1.1/header#independentHeader"><span class="headingNumber">2.6
                                 </span><span class="head">Independent Headers</span></a></li>
                        <li><a href="/documentation/2.1.1/header#independentHeaderDefinition"><span class="headingNumber">2.6.1 </span><span class="head">Definition and Principles for
                                 Encoders</span></a></li>
                        <li><a href="/documentation/2.1.1/header#biblAnalog"><span class="headingNumber">2.6.2
                                 </span><span class="head">Header Elements and their Relationship to Other
                                 Bibliographic Standards</span></a></li>
                        <li><a href="/documentation/2.1.1/header#relatedItemVsFRBR"><span class="headingNumber">2.7 </span><span class="head">RelatedItem vs. FRBR</span></a></li>
                     </ul>
                  </div>
               </div>
            </div>
         </div>
      </div>
   </article>
</div>