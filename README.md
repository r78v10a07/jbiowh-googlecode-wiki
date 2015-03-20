#summary Summary description about the JBioWH framework

The _*Java Biological Warehouse*_ (*JBioWH*) is a mature computational system which provides a framework for biological data integration and management. The system is based in a relational schema to integrate the most important public biological data sources into a [RelationalSchema relational schema] and a [JavaAPI Java API] to support rapid bioinformatics application development. Also, we developed a [DesktopTool Desktop Tool] which contains an extended search interface and a [SQLEditor SQL Editor Tab] to interact with the database. 

*JBioWH* provides a framework for biological data integration and management which contains a relational schema for biological data integration, a java *Application Programming Interface* (*API*) and a powerful Desktop tool. 

This framework is designed to provide 
  # data warehouse capabilities to integrate and normalize non heterogeneous biological data
  # an extensive desktop tool for a scientist with no programming experience including an advanced SQL editor for scientist with this programming skill, and, 
  # a java API to handle the integrated biological data for further development of Bioinformatics tools.
 
The [RelationalSchema relational database schema] includes the following data sources types: *Taxonomy*, *Ontology*, *Gene*, *Genomes*, *Protein*, *Enzymes*, *Metabolites* (compound and glycan), *Reactions*, *Protein-Protein Interactions*, *Protein clusters*, *Drug-Target interactions*, *Pathways*, *Diseases* and *Domains* provided by public available biological data sources. 

The [JavaAPI Java API] includes the parser to extract and insert the biological data from its original data sources file format into the relational database schema. Also, includes the entities and controller classes to use the inserted information on Java programs.

Read this [UseInExternalProject tutorial ] to integrate in your own JPA model the *JBioWH* relational schema. 

This project is supported by the [http://www.icgeb.trieste.it International Centre for Genetic Engineering and Biotechnology (ICGEB)] under its "Sandwich" PhD Programme.

A free MySQL server is available for testing.

{{{
Server: hydrax.icgeb.trieste.it
Port: 3307
User: biowh
Password: mypass
}}}

The following figure shows the relationship between the JBioWH modules.

<img src="https://raw.githubusercontent.com/r78v10a07/jbiowh-googlecode-wiki/master/images/EntitiesRelationship.png"

The table shows a report for the biological databases used by the JBioWH framework. This example was executed in a computer with two [http://www.cpu-world.com/CPUs/K8/AMD-Opteron%20240%20-%20OSADA240CCO5.html AMD Opteron Processor 240] (1.4 GHz and 1.0 MB of cache) and 4.0 GB of RAM running OpenSuSE 12.2 (Linux version 3.4.28-2.20-desktop, SMP PREEMPT Tue Jan 29 16:51:37 UTC 2013 (143156b)). 

<table border="1">
<tr>
<th>DB</th>
<th>Download Date</th>
<th>File size (MB)</th>
<th>MySQL size (MB)</th>
<th>Load time (2)</th>
<th>No. main elements</th>
<th>No. elements</th>
</tr>
<tr>
<td>[TaxonomyCF NCBI Taxonomy]</td>
<td align="center">03/05/13</td>
<td align="right">157.0</td>
<td align="right">546.97</td>
<td align="right">395</td>
<td align="right">985 849</td>
<td align="right">2 732 658</td>
</tr>
<tr>
<td>[OntologyCF GO Ontology]</td>
<td align="center">03/05/13</td>
<td align="right">3.7</td>
<td align="right">70.07</td>
<td align="right">56</td>
<td align="right">38 794</td>
<td align="right">468 870</td>
</tr>
<tr>
<td>[GeneCF Gene]</td>
<td align="center">03/05/13</td>
<td align="right">5 619.0</td>
<td align="right">14 801.00</td>
<td align="right">7 252</td>
<td align="right">11 200 928</td>
<td align="right">90 459 357</td>
</tr>
<tr>
<td>[GenomesPTTCF Complete Genomes]</td>
<td align="center">03/05/13</td>
<td align="right">577.0</td>
<td align="right">2 055.00</td>
<td align="right">4 658</td>
<td align="right">7 192 870</td>
<td align="right">7 195 133</td>
</tr>
<tr>
<td>[GenomesPTTCF Draft Genomes]</td>
<td align="center">03/11/13</td>
<td align="right">3 130.0</td>
<td align="right">6 143.00</td>
<td align="right">48 084</td>
<td align="right">17 166 166</td>
<td align="right">17 168 429</td>
</tr>
<tr>
<td>[ProteinCF UniProt (SwissProt)]</td>
<td align="center">03/11/13</td>
<td align="right">737.0</td>
<td align="right">4 228.00</td>
<td align="right">4 374</td>
<td align="right">538 849</td>
<td align="right">50 827 445</td>
</tr>
<tr>
<td>[ProteinCF UniProt (TREMBL)]</td>
<td align="center">03/05/13</td>
<td align="right">21 953.0</td>
<td align="right">131 352.00</td>
<td align="right">253 304</td>
<td align="right">29 266 939</td>
<td align="right">1 056 770 378</td>
</tr>
<tr>
<td>[ProtFamCF UniRef 90]</td>
<td align="center">03/12/13</td>
<td align="right">4 379.0</td>
<td align="right">25 787.00</td>
<td align="right">41 536</td>
<td align="right">13 195 411</td>
<td align="right">285 706 680</td>
</tr>
<tr>
<td>[MIF25CF IntAct]</td>
<td align="center">03/12/13</td>
<td align="right">2 757.0</td>
<td align="right">2 579.00</td>
<td align="right">895</td>
<td align="right">6 234</td>
<td align="right">14 851 480</td>
</tr>
<tr>
<td>[MIF25CF BioGrid]</td>
<td align="center">03/12/13</td>
<td align="right">2 598.0</td>
<td align="right">2 053.00</td>
<td align="right">2 603</td>
<td align="right">1</td>
<td align="right">15 583 825</td>
</tr>
<tr>
<td>[MIF25CF DIP]</td>
<td align="center">03/12/13</td>
<td align="right">164.0</td>
<td align="right">280.00</td>
<td align="right">306</td>
<td align="right">1</td>
<td align="right">1 833 668</td>
</tr>
<tr>
<td>[MIF25CF MINT]</td>
<td align="center">03/12/13</td>
<td align="right">990.0</td>
<td align="right">15 466.00</td>
<td align="right">1 103</td>
<td align="right">1 400</td>
<td align="right">4 394 018</td>
</tr>
<tr>
<td>[DiseaseCF OMIM]</td>
<td align="center">03/12/13</td>
<td align="right">163.0</td>
<td align="right">332.00</td>
<td align="right">419</td>
<td align="right">22 750</td>
<td align="right">874 906</td>
</tr>
<tr>
<td>[DomainCF PFAM]</td>
<td align="center">03/12/13</td>
<td align="right">31 000.0</td>
<td align="right">20 501.00</td>
<td align="right">27 132</td>
<td align="right">13 672</td>
<td align="right">154 792 451</td>
</tr>
<tr>
<td>[DrugBankCF DrugBank]</td>
<td align="center">03/12/13</td>
<td align="right">90.0</td>
<td align="right">143.00</td>
<td align="right">95</td>
<td align="right">6 711</td>
<td align="right">397 847</td>
</tr>
<tr>
<td>[PathwayCF KEGG]</td>
<td align="center">06/11/11</td>
<td align="right">40 668.0</td>
<td align="right">14 784.00</td>
<td align="right">54 380</td>
<td align="right">126 478</td>
<td align="right">130 479 471</td>
</tr>
<tr>
<th>Total (GB and Hours)</th>
<th> </th>
<th align="right">112.29</th>
<th align="right">235.47</th>
<th align="right">124.05</th>
<th align="right">79 763 053</th>
<th align="right">1 834 536 616</th>
</tr>
</table>

Please use the <a href="http://groups.google.com/group/jbiowh-discuss">JBioWH Google Group</a> to discuss, or to post questions. 
