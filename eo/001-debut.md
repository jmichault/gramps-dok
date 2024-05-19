---
kategorio: Prezento
lang: eo
lang-niv: fonto
lang-ref: 001-debut
layout: page
mermaid: true
title: 'Simpligitaj datumaj diagramoj'
---

Antaŭ ol eniri Gramps, gravas kompreni kiel la datumoj estas organizitaj. 

# La familia universo

La tri esencaj objektoj, kiuj permesos al vi konstrui vian arbon, estas:
* la individuo:   
  la bazo de via genealogio.   
* la familio : 
  Familio en Gramps konsistas el unu aŭ du individuoj \(konvencie la edzo kaj la virino, sed Gramps rajtigas ĉiujn kombinaĵojn\), kaj infanojn. Ĝi permesos konstrui la arbon.
* la evento:  
  okazaĵo konsistas ĉefe el tipo, dato \(aŭ pèriodo\), kaj priskribo.   
  Ekzemple naskiĝo, deklaro de naskiĝo, morto, geedzeco, la profesio estos kaptita en evento. 
  La evento povas esti referencita de individuoj kaj/aŭ familioj.

<div class="mermaid">
   erDiagram
     Familio ||--o| Individuo: "Edzo/edzo"
     Familio ||--o| Individuo: "Virino/edzo"
     Familio ||--o{ Individuo: "Infanoj"
     Familio ||--o{ "Okazaĵoj": participo
     Individuo ||--o{ "Okazaĵoj": participo
     Individuo{
       Nomo Cxefa_Nomo
       Nomlisto Alternativaj_Nomoj
     }
     Familio{
       Teksto Tipo
     }
     "Okazaĵoj"{
       Teksto Tipo
       Dato Event_date
       Tekste Priskribo
       Loko loko_de_la_okazajxo
     }

</div>

# La universo de fontoj
Fontaĵi vian genealogion estas esenca por ĝia validigo.   
Vi havas tri objektojn por administri la fontojn:
* la citaĵo:  
  Ĉi tiu estas la plej bona elemento de fontoj, tiu, kiu estos referencita de la individuo, la familio, la evento, la loko, la aŭdvidaĵo.   
  Ekzemple ĝi estos la naskiĝtesto trovita en registro, alineo en libro aŭ revuo ...
  La citaĵo estas ligita al fonto.  
* la fonto :  
  La fonto estas la medio el kiu vi ĉerpas viajn citaĵojn.   
  Ĝi povas esti registro, mikrofilmo, libro ...
La fonto situas en unu aŭ pluraj kuŝejoj.
* la deponejoj:  
  La deponejo ebligas grupigi la fontojn.   
  Ĝi povas esti faka arkivo, retejo, via monŝranko...  
  Fonto troveblas en pluraj deponejoj.   
  Bedaŭrinde, la hierarkio de fontoj finiĝas tie. Oni eble volas, ke deponejo estu parto de alia deponejo, sed gramps ne subtenas ĉi tion.
<div class="mermaid">
   erDiagram
     "Cita&jcirc;o" ||--o| Fonto: en
     Fonto ||--o{ "Deponejo": "konservita en (subtena tipo, takso)"
     "Cita&jcirc;o"{
       Dato dato_de_okazajxo
       Volumo_Pagxo loko_en_fonto
       nivelo konfido_nivelo
     }
     Fonto{
       Teksto Titolo
       Teksto Auxtoroj
       Teksto Publikigo_info
       Teksto Mallongigo
     }
     "Deponejo"{
       Teksto Nomo
       Teksto Tipo
       Adreso Adreso
       listo_de_ligiloj Interretaj_ligiloj
     }
</div>

# Aneksitaj objektoj
Fine kvar objektoj por riĉigi viajn datumojn:
* la aŭdvidaĵo:  
   Permesas al vi integri dosieron en la arbon. Ĝi povas esti bildo, video, PDF aŭ io alia.  
   Ni povos ligi ĝin al individuoj, familioj, eventoj, citaĵoj aŭ lokoj.   
* la noto : 
   formita de titolo kaj teksto\(multiligna kaj formatinda\).  
   Tre utila! Povas esti ligita al iu ajn objekto aŭ objektoreferenco.
   Permesas al vi enigi la enhavon de dokumentoj, enigi serĉajn kondukojn kaj multajn aliajn aferojn.
   Noto povas esti ligita al pluraj objektoj.
* loko: 
  Por ne re -enigi la samon, evitu kopii erarojn, specife lokalizi la lokojn, kie okazis viaj eventoj.   
  La lokoj povas kuniĝi unu en la alia \(Ekzemplo: lando-> fako-> municipo-> vilaĝeto\).   
  Antaŭ ol vi komencas eniri lokojn, vi devas zorge pripensi kiel vi organizas la lokojn, kaj kiu kromaĵo permesos al vi administri ilin.
* la etikedo
  Ili povas esti administritaj per la menuo "Redaktu" --> "Etikedo".  
  Vi povas meti etikedojn sur ĉiu objekto.  
  Etikedo estas mallonga teksto, kun kiu oni asocias koloron.   
  La etikedoj povas esti uzataj:
  * por filtri
  * por reliefigi en la listoj aŭ en la grafika vido, danke al la koloro. 

# la kompleta diagramo
Se vi volas iri pli detale, la diagramo de la datumbazo Gramps povas esti konsultita ĉi tie: <https://gramps-project.org/wiki/index.php/Gramps_Data_model>


# Unuaj Kaptiloj
## krei individuon
## aldonu eventon al individuo
## aldonu gepatrojn
## aldonu edzinon
## aldonu infanon
## aldonu Citaĵon

# Iru plie
## lokoj
## la notoj
## la glumarkoj
## la aŭdvidaĵoj


# Kie ricevi helpon?
* oficiala Dokumentado: <https://gramps-project.org/wiki/index.php/Gramps_5.1_Wiki_Manual>

* gramps Diskurso: <https://gramps.discourse.group/> \(en la angla\)

* la forumo de geneanet: <https://www.geneanet.org/forum/viewforum.php?f=55945&sid=de725cd97855d4a68268a420061b629f> \(en la franca\)

