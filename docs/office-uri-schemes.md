---
title: Esquemas URI de Office
manager: luken
ms.date: 01/14/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1ea99a8f-b005-4b92-b313-923294d20fbf
ms.openlocfilehash: 246c1da3647b61c6281c1a52a24826b3f22e5d7e
ms.sourcegitcommit: 939bd9686ba41a8f94b82e004ed84b9054d9c7cf
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2020
ms.locfileid: "48293502"
---
# <a name="office-uri-schemes"></a>Esquemas URI de Office

## <a name="11-abstract"></a>1.1 RESUMEN

Este documento define el formato de los identificadores uniformes de recursos (URI) para las aplicaciones de productividad de Office. Se admite el esquema en el Service Pack 2 de Microsoft Office 2010 y versiones posteriores, incluidos Microsoft Office 2013 para Windows y los productos de Microsoft SharePoint 2013. También se admite en Office para iPhone, Office para iPad y Office para Mac 2011.
  
## <a name="12-introduction"></a>1.2 INTRODUCCIÓN

Estos esquemas URI permiten invocar con diversos comandos las aplicaciones de productividad de Office. Cada aplicación recibe un esquema con nombre diferente, pero todos los esquemas siguen las mismas reglas para la formación de URI (esquema URI).
  
## <a name="13-uri-schema"></a>1.3 ESQUEMA URI

### <a name="full-schema"></a>Esquema completo

< *nombre-esquema*  >:<  *nombre-comando*  >"|"<  *descriptor-argumento-comando*  > "|"<  *argumento-comando*  > 
  
Un URI, tal y como se define en este documento puede tener un argumento de comando o más, cada uno de los cuales debe incluir los elementos < *descriptor-argumento-comando*  > y el <  *argumento-comando*  > y debe estar delimitado con el carácter de barra vertical ("|"). Cuando se incluye un argumento de comando o más en un URI, debe haber un carácter de barra vertical ("|") para separar cada argumento de comando del argumento de comando siguiente. 
  
Estos esquemas no incluyen un componente de la entidad emisora tal como se define en la sección 3.2 de RFC 3986. La invocación de los comandos especificados en este documento se realiza en el contexto del sistema al invocar el comando. Por ejemplo, cuando se invoca el URI "ms-excel:ofv|u|https://contoso/Q4/budget.xls" desde un equipo que tiene Microsoft Windows con Microsoft Office 2013 instalado, el resultado que se espera es que se ejecutará la instalación local de Microsoft Excel y se pasarán argumentos para abrir el archivo en  *https://contoso/Q4/budget.xls*  en modo de solo lectura. Tenga en cuenta que la barra vertical que se usa como delimitador de esta especificación no se encuentra entre los caracteres identificados en la sección 2.2 de RFC 3986 porque está reservado para uso potencial como delimitadores. Esto se hace intencionalmente para maximizar el conjunto de caracteres que el argumento de comando URI puede admitir sin necesidad de codificar los caracteres con porcentaje. 
  
La sintaxis de esquema incluye lo siguiente:
  
1. < *nombre-esquema*  >: Hace referencia al tipo de aplicación que se debe invocar. Por ejemplo, el nombre del esquema ms-word se registra con Microsoft Word. 
    
2. Separador ":"
    
3. < *nombre-comando*  >: Describe las acciones que debe realizar la aplicación. Por ejemplo, abrir un documento para su visualización. La lista de nombres de comando se describe en la sección 1.5. 
    
4. Separador "|" (barra vertical)
    
5. < *descriptor-argumento-comando*  >: Este elemento proporciona más información sobre el argumento del comando. 
    
6. Separador "|" (barra vertical)
    
7. < *argumento-comando*  >: Los argumentos varían según el comando. Un argumento común es el URI para un documento, normalmente mediante el esquema http o https. Tenga en cuenta que dentro de los segmentos <  *argumento-comando*  > los caracteres reservados RFC 3986 ":" y "/" forman parte de los datos del argumento, no los delimitadores y por lo tanto, se incluyen sin secuencias de escape. 
    
### <a name="abbreviated-schema"></a>Esquema abreviado

An abbreviated form of the office URI schemes allows for a more compact request to launch a specified Office application to open the resource located at a given URI. This abbreviated form implies the < *command-name*  > "ofv" and the <  *command-argument-descriptor*  > "u". No further commands or command arguments are allowed in this schema. 
  
< *nombre-esquema*  >:<  *argumento-comando*  > 
  
1. < *nombre-esquema*  >: El tipo de aplicación que se debe invocar. Por ejemplo, ms-word: para Microsoft Word. 
    
2. < *argumento-comando*  >: URI para el recurso que la aplicación debe abrir. Se admiten URI únicos basados en esquemas http o https. 
    
## <a name="14-scheme-names-and-office-application-registrations"></a>1.4 NOMBRES DE ESQUEMAS Y REGISTROS DE APLICACIONES DE OFFICE

La siguiente es la lista de nombres de esquemas implementados en aplicaciones de Microsoft Office. Cuando se instala Microsoft Office, se registra cada nombre del esquema con Windows para ser controlado por el producto de Office del mismo nombre. Tenga en cuenta que "ms-spd" es una abreviatura de SharePoint Designer.
  
> - *ms-word:* 
    
> - *ms-powerpoint:* 
    
> - *ms-excel:* 
    
> - *ms-visio:* 
    
> - *ms-access:* 
    
> - *ms-project:* 
    
> - *ms-publisher:* 
    
> - *ms-spd:* 
    
> - *ms-infopath:* 
    
## <a name="15-commands-and-required-command-arguments"></a>1.5 COMANDOS Y ARGUMENTOS DE COMANDO NECESARIOS

### <a name="view-document"></a>Ver documento

El siguiente comando hará que la aplicación abra el documento al que hace referencia el URI en modo de solo lectura o vista.
  
> Nombre del comando: ofv
    
> Descriptor de argumento de comando: u
    
> Argumento de comando: Un URI para el documento, según el esquema http o https
    
> Ejemplo:  *ms-excel:ofv|u|https://contoso/Q4/budget.xls* 
    
### <a name="edit-document"></a>Editar documento

El siguiente comando hará que la aplicación abra el documento al que hace referencia el URI en modo de edición
  
> Nombre del comando: ofe
    
> Descriptor de argumento de comando: u
    
> Argumento de comando: Un URI para el documento, según el esquema http o https
    
> Ejemplo:  *ms-powerpoint:ofe|u|https://www.fourthcoffee.com/AllHandsDeck.ppt* 
    
### <a name="new-document-from-template"></a>Nuevo documento de plantilla

El siguiente comando hará que la aplicación cree y abra un nuevo documento según la plantilla almacenada en el URI especificado. No se modifica el archivo de plantilla en este proceso. Puede proporcionarse un argumento de comando adicional para especificar la ruta predeterminada ofrecida como ubicación de guardado cuando se guarda el archivo por primera vez. Es posible que el usuario elija una ubicación diferente.
  
> Nombre del comando: nft
    
> Descriptor de argumento de comando 1: u
    
> Argumento de comando 1: Un URI para la plantilla, según el esquema http o https
    
> Descriptor de argumento de comando opcional 2: s
    
> Argumento de comando opcional 2: URI para especificar la carpeta de guardado predeterminada
    
> Ejemplo:  *ms-word:nft|u|https://cohowinery/templates/elegance.pot|s|https://cohowinery/presentations* 
    
Como nota, si se proporciona la ubicación de guardado predeterminada opcional, debe estar apuntando al mismo nombre de host que la plantilla.
  
Además, las aplicaciones de SharePoint Designer e InfoPath (que implementan el esquema ms-spd: y los esquemas ms-infopath:, respectivamente) no admiten la funcionalidad "nuevo documento de plantilla".
  
## <a name="16-backwards-compatibility"></a>1.6 COMPATIBILIDAD CON VERSIONES ANTERIORES

Al analizar un URI para extraer los argumentos de comando adecuados para un comando determinado, el controlador URI de Office solo usará los argumentos de comando que tengan el descriptor de argumento de comando esperado. Si hay pares adicionales de argumentos y descriptores de argumentos que tengan descriptores de argumento inesperados, se quitarán del URI. Este mecanismo permite que las versiones futuras del esquema agreguen argumentos de comando adicionales sin interrumpir la compatibilidad con implementaciones heredadas de este esquema.
  
## <a name="17-implementation-restrictions-on-command-arguments"></a>1.7 RESTRICCIONES DE IMPLEMENTACIÓN EN ARGUMENTOS DE COMANDO

Se colocan las siguientes restricciones en argumentos de comando en su implementación actual de Office 2013.
  
### <a name="length-limitations-on-uri-command-arguments"></a>Limitaciones de longitud en argumentos de comando URI

Para argumentos de comando URI, la longitud de ruta máxima es de 256 caracteres para todas las aplicaciones excepto Excel, donde el límite es de 216. Se pueden admitir longitudes de ruta mayores que estas según cada aplicación individual, y se recomienda realizar una prueba antes de implementar las soluciones que dependen de esto.
  
### <a name="allowed-characters-in-uri-command-arguments"></a>Caracteres permitidos en argumentos de comando URI

Los URI permitidos deben cumplir con los estándares propuestos en RFC 3987: Identificadores de recursos internacionalizados (IDI). Los caracteres identificados como reservados en RFC 3986 no deben codificarse por porcentaje. . Los nombres de archivo no deben contener ninguno de los siguientes caracteres: \ / : ? \< \> | " o \* .  
  
## <a name="appendix-a---uri-scheme-registration-template-for-ms-word-scheme"></a>APÉNDICE A: PLANTILLA DE REGISTRO DE ESQUEMA URI PARA ESQUEMA MS-WORD
<a name="bk_addresources"> </a>

### <a name="a-3-uri-scheme-syntax"></a>A-3. Sintaxis de esquema URI

> Esquema de Word = "ms-word:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd
    
> open-for-edit-cmd = "ofe|u|" document-uri
    
> open-for-view-cmd = "ofv|u|" document-uri
    
> new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]
    
> document-uri = ubicación URI de documento para abrir
    
> template-uri = ubicación URI de archivo de plantilla que se usará para el nuevo archivo
    
> save-location = ubicación URI de carpeta en la que se creará el nuevo documento
    
### <a name="a-4-uri-scheme-semantics"></a>A-4. Semántica de esquema URI

El esquema ms-word define una sintaxis URI para abrir o crear un documento de procesador de texto. El esquema define tres comandos que sirven como instrucciones sobre qué se debe hacer con el documento de referencia. Los comandos son 1) open-for-edit-cmd (ofe), que indica a un procesador de texto que abra el documento en el URI especificado para la edición; 2) open-for-view-cmd (ofv), que indica a un procesador de texto que abra el documento en el URI especificado en modo de solo lectura; y 3) new-from-template-cmd (nft), que indica a un procesador de texto que cree un nuevo documento según la plantilla de documento ubicada en el URI template-uri especificado y guarde el nuevo documento en la ubicación especificada en el URI save-location opcional o, si falta el URI opcional, en la ubicación de la biblioteca de documentos predeterminada.
  
### <a name="a-5-applicationsprotocols-that-use-the-ms-word-uri-scheme"></a>A-5. Aplicaciones/protocolos que usan el esquema URI ms-word

Microsoft Office 2013 usa el esquema URI ms-word para invocar Microsoft Word 2013 o Microsoft Word 2010 con Service Pack 2. Microsoft SharePoint 2013 usa URI ms-word como vínculos a documentos de procesador de texto almacenados en bibliotecas de documentos de SharePoint.
  
### <a name="a-6-interoperability-considerations"></a>A-6. Consideraciones de interoperabilidad

Tenga en cuenta que la barra vertical que se usa como delimitador de esta especificación no se encuentra entre los caracteres identificados en la sección 2.2 de RFC 3986 porque está reservado para uso potencial como delimitadores. Esto se hace intencionalmente para maximizar el conjunto de caracteres que el argumento de comando URI puede admitir sin necesidad de codificar los caracteres con porcentaje.
  
Dentro de los segmentos < *argumento-comando*  > los caracteres reservados RFC 3986 ":" y "/" forman parte de los datos del argumento, no los delimitadores y por lo tanto, se incluyen sin secuencias de escape. 
  
### <a name="a-7-security-considerations"></a>A-7. Consideraciones de seguridad

 En sistemas que tienen controladores registrados para reconocer y actuar en URI ms-word, al hacer clic en un vínculo a un URI ms-word, el procesador de texto registrado se iniciará, con instrucciones de que el procesador de texto intente abrir un documento en el URI especificado. Los procesadores de texto que se registran para procesar URI ms-word deben implementar protecciones para protegerse contra la apertura de documentos desde sistemas remotos que no son de confianza y que pueden incluir código malintencionado. 
  
### <a name="a-8-references"></a>A-8. Referencias

RFC 3987: Identificadores de recursos internacionales (IRI)  
  
## <a name="appendix-b---uri-scheme-registration-template-for-ms-powerpoint-scheme"></a>APÉNDICE B: PLANTILLA DE REGISTRO DE ESQUEMA URI PARA ESQUEMA MS-POWERPOINT
<a name="bk_addresources"> </a>

### <a name="b-3-uri-scheme-syntax"></a>B-3. Sintaxis de esquema URI

- Esquema de PowerPoint = "ms-powerpoint:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd
    
- open-for-edit-cmd = "ofe|u|" document-uri
    
- open-for-view-cmd = "ofv|u|" document-uri
    
- new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]
    
- document-uri = ubicación URI de documento para abrir
    
- template-uri = ubicación URI de archivo de plantilla que se usará para el nuevo archivo
    
- save-location\* = ubicación URI de carpeta en la que se creará el nuevo documento
    
- \*save-location es un parámetro opcional
    
### <a name="b-4-uri-scheme-semantics"></a>B-4. Semántica del esquema URI

El esquema ms-powerpoint define una sintaxis URI para abrir o crear un documento de presentación. El esquema define tres comandos que sirven como instrucciones sobre qué se debe hacer con el documento de referencia. Los comandos son 1) open-for-edit-cmd (ofe), que indica a una aplicación de presentación que abra el documento en el URI especificado para la edición; 2) open-for-view-cmd (ofv), que indica a una aplicación de presentación que abra el documento en el URI especificado en modo de solo lectura; y 3) new-from-template-cmd (nft), que indica a una aplicación de presentación que cree un nuevo documento según la plantilla de documento ubicada en el URI template-uri especificado y guarde el nuevo documento en la ubicación especificada en el URI save-location opcional o, si falta el URI opcional, en la ubicación de la biblioteca de documentos predeterminada.
  
### <a name="b-5-applicationsprotocols-that-use-the-ms-powerpoint-uri-scheme"></a>B-5. Aplicaciones/protocolos que usan el esquema URI ms-powerpoint

Microsoft Office 2013 usa el esquema URI ms-powerpoint para invocar Microsoft PowerPoint 2013 o Microsoft PowerPoint 2010 con Service Pack 2. Microsoft SharePoint 2013 usa URI ms-powerpoint como vínculos a documentos de presentación almacenados en bibliotecas de documentos de SharePoint.
  
### <a name="b-6-interoperability-considerations"></a>B-6. Consideraciones de interoperabilidad

Tenga en cuenta que la barra vertical que se usa como delimitador de esta especificación no se encuentra entre los caracteres identificados en la sección 2.2 de RFC 3986 porque está reservado para uso potencial como delimitadores. Esto se hace intencionalmente para maximizar el conjunto de caracteres que el argumento de comando URI puede admitir sin necesidad de codificar los caracteres con porcentaje.
  
Dentro de los segmentos < *argumento-comando*  > los caracteres reservados RFC 3986 ":" y "/" forman parte de los datos del argumento, no los delimitadores y por lo tanto, se incluyen sin secuencias de escape. 
  
### <a name="b-7-security-considerations"></a>B-7. Consideraciones de seguridad

En sistemas que tienen controladores registrados para reconocer y actuar en URI ms-powerpoint, al hacer clic en un vínculo a un URI ms-powerpoint, la aplicación de presentación registrada se iniciará, con instrucciones de que la aplicación intente abrir un documento en el URI especificado. Las aplicaciones que se registran para procesar URI ms-powerpoint deben implementar protecciones para protegerse contra la apertura de documentos desde sistemas remotos que no son de confianza y que pueden incluir código malintencionado.
  
### <a name="b-8-references"></a>B-8. Referencias

RFC 3987: Identificadores de recursos internacionales (IRI)  
  
## <a name="appendix-c---uri-scheme-registration-template-for-ms-excel-scheme"></a>APÉNDICE C: PLANTILLA DE REGISTRO DE ESQUEMA URI PARA ESQUEMA MS-EXCEL
<a name="bk_addresources"> </a>

### <a name="c-3-uri-scheme-syntax"></a>C-3. Sintaxis de esquema URI

> Esquema de Excel = "ms-excel:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd
    
> open-for-edit-cmd = "ofe|u|" document-uri
    
> open-for-view-cmd = "ofv|u|" document-uri
    
> new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]
    
> document-uri = ubicación URI de documento para abrir
    
> template-uri = ubicación URI de archivo de plantilla que se usará para el nuevo archivo
    
> save-location\* = ubicación URI de carpeta en la que se creará el nuevo documento
    
> \*save-location es un parámetro opcional
    
### <a name="c-4-uri-scheme-semantics"></a>C-4. Semántica del esquema URI

El esquema ms-excel define una sintaxis URI para abrir o crear un documento de hoja de cálculo. El esquema define tres comandos que sirven como instrucciones sobre qué se debe hacer con el documento de referencia. Los comandos son 1) open-for-edit-cmd (ofe), que indica a una aplicación de hoja de cálculo que abra el documento en el URI especificado para la edición; 2) open-for-view-cmd (ofv), que indica a una aplicación de hoja de cálculo que abra el documento en el URI especificado en modo de solo lectura; y 3) new-from-template-cmd (nft), que indica a una aplicación de hoja de cálculo que cree un nuevo documento según la plantilla de documento ubicada en el URI template-uri especificado y guarde el nuevo documento en la ubicación especificada en el URI save-location opcional o, si falta el URI opcional, en la ubicación de la biblioteca de documentos predeterminada.
  
### <a name="c-5-applicationsprotocols-that-use-the-ms-excel-uri-scheme"></a>C-5. Aplicaciones/protocolos que usan el esquema URI ms-excel

Microsoft Office 2013 usa el esquema URI ms-excel para invocar Microsoft Excel 2013 o Microsoft Excel 2010 con Service Pack 2. Microsoft SharePoint 2013 usa URI ms-excel como vínculos a documentos de hoja de cálculo almacenados en bibliotecas de documentos de SharePoint.
  
### <a name="c-6-interoperability-considerations"></a>C-6. Consideraciones de interoperabilidad

Tenga en cuenta que la barra vertical que se usa como delimitador de esta especificación no se encuentra entre los caracteres identificados en la sección 2.2 de RFC 3986 porque está reservado para uso potencial como delimitadores. Esto se hace intencionalmente para maximizar el conjunto de caracteres que el argumento de comando URI puede admitir sin necesidad de codificar los caracteres con porcentaje.
  
Dentro de los segmentos < *argumento-comando*  > los caracteres reservados RFC 3986 ":" y "/" forman parte de los datos del argumento, no los delimitadores y por lo tanto, se incluyen sin secuencias de escape. 
  
### <a name="c-7-security-considerations"></a>C-7. Consideraciones de seguridad

En sistemas que tienen controladores registrados para reconocer y actuar en URI ms-excel, al hacer clic en un vínculo a un URI ms-excel, la aplicación de hoja de cálculo registrada se iniciará, con instrucciones de que la aplicación intente abrir un documento en el URI especificado. Las aplicaciones que se registran para procesar URI ms-excel deben implementar protecciones para protegerse contra la apertura de documentos desde sistemas remotos que no son de confianza y que pueden incluir código malintencionado.
  
### <a name="c-8-references"></a>C-8. Referencias

RFC 3987: Identificadores de recursos internacionales (IRI)  
  
## <a name="appendix-d---uri-scheme-registration-template-for-ms-visio-scheme"></a>APÉNDICE D: PLANTILLA DE REGISTRO DE ESQUEMA URI PARA ESQUEMA MS-VISIO
<a name="bk_addresources"> </a>

### <a name="d-3-uri-scheme-syntax"></a>D-3. Sintaxis de esquema URI

> Esquema de Visio = "ms-visio:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd
    
> open-for-edit-cmd = "ofe|u|" document-uri
    
> open-for-view-cmd = "ofv|u|" document-uri
    
> new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]
    
> document-uri = ubicación URI de documento para abrir
    
> template-uri = ubicación URI de archivo de plantilla que se usará para el nuevo archivo
    
> save-location\* = ubicación URI de carpeta en la que se creará el nuevo documento
    
> \*save-location es un parámetro opcional
    
### <a name="d-4-uri-scheme-semantics"></a>D-4. Semántica de esquema URI

El esquema ms-visio define una sintaxis URI para abrir o crear un documento de Microsoft Visio. El esquema define tres comandos que sirven como instrucciones sobre qué se debe hacer con el documento de referencia. Los comandos son 1) open-for-edit-cmd (ofe), que indica a Visio que abra el documento en el URI especificado para la edición; 2) open-for-view-cmd (ofv), que indica a Visio que abra el documento en el URI especificado en modo de solo lectura; y 3) new-from-template-cmd (nft), que indica a Visio que cree un nuevo documento según la plantilla de documento ubicada en el URI template-uri especificado y guarde el nuevo documento en la ubicación especificada en el URI save-location opcional o, si falta el URI opcional, en la ubicación de la biblioteca de documentos predeterminada.
  
### <a name="d-5-applicationsprotocols-that-use-the-ms-visio-uri-scheme"></a>D-5. Aplicaciones/protocolos que usan el esquema URI ms-visio

Microsoft Office 2013 usa el esquema URI ms-visio para invocar Microsoft Visio 2013 o Microsoft Visio 2010 con Service Pack 2. Microsoft SharePoint 2013 usa URI ms-visio como vínculos a documentos de Visio almacenados en bibliotecas de documentos de SharePoint.
  
### <a name="d-6-interoperability-considerations"></a>D-6. Consideraciones de interoperabilidad

Tenga en cuenta que la barra vertical que se usa como delimitador de esta especificación no se encuentra entre los caracteres identificados en la sección 2.2 de RFC 3986 porque está reservado para uso potencial como delimitadores. Esto se hace intencionalmente para maximizar el conjunto de caracteres que el argumento de comando URI puede admitir sin necesidad de codificar los caracteres con porcentaje.
  
Dentro de los segmentos < *argumento-comando*  > los caracteres reservados RFC 3986 ":" y "/" forman parte de los datos del argumento, no los delimitadores y por lo tanto, se incluyen sin secuencias de escape. 
  
### <a name="d-7-security-considerations"></a>D-7. Consideraciones de seguridad

En sistemas que tienen controladores registrados para reconocer y actuar en URI ms-visio, al hacer clic en un vínculo a un URI ms-visio, la aplicación registrada se iniciará, con instrucciones de que la aplicación intente abrir un documento en el URI especificado. Las aplicaciones que se registran para procesar URI ms-visio deben implementar protecciones para protegerse contra la apertura de documentos desde sistemas remotos que no son de confianza y que pueden incluir código malintencionado.
  
### <a name="d-8-references"></a>D-8. Referencias

RFC 3987: Identificadores de recursos internacionales (IRI)
  
## <a name="appendix-e---uri-scheme-registration-template-for-ms-access-scheme"></a>APÉNDICE E: PLANTILLA DE REGISTRO DE ESQUEMA URI PARA ESQUEMA MS-ACCESS
<a name="bk_addresources"> </a>

### <a name="e-3-uri-scheme-syntax"></a>E-3. Sintaxis de esquema URI

> Esquema de Access = "ms-access:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd
    
> open-for-edit-cmd = "ofe|u|" document-uri
    
> open-for-view-cmd = "ofv|u|" document-uri
    
> new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]
    
> document-uri = ubicación URI de documento para abrir
    
> template-uri = ubicación URI de archivo de plantilla que se usará para el nuevo archivo
    
> save-location\* = ubicación URI de carpeta en la que se creará el nuevo documento
    
> \*save-location es un parámetro opcional
    
### <a name="e-4-uri-scheme-semantics"></a>E-4. Semántica de esquema URI

El esquema ms-access define una sintaxis URI para abrir o crear una base de datos. El esquema define tres comandos que sirven como instrucciones sobre qué se debe hacer con el archivo de base de datos de referencia. Los comandos son 1) open-for-edit-cmd (ofe), que indica a una aplicación de base de datos que abra la base de datos en el URI especificado para la edición; 2) open-for-view-cmd (ofv), que indica a una aplicación de base de datos que abra la base de datos en el URI especificado en modo de solo lectura; y 3) new-from-template-cmd (nft), que indica a la aplicación de base de datos que cree una nueva base de datos según la plantilla ubicada en el URI template-uri especificado y guarde la nueva base de datos en la ubicación especificada en el URI save-location opcional o, si falta el URI opcional, en la ubicación de la biblioteca de documentos predeterminada.
  
### <a name="e-5-applicationsprotocols-that-use-the-ms-access-uri-scheme"></a>E-5. Aplicaciones/protocolos que usan el esquema URI ms-access

Microsoft Office 2013 usa el esquema URI ms-access para invocar Microsoft Access 2013 o Microsoft Access 2010 con Service Pack 2 desde páginas web. Microsoft SharePoint 2013 usa URI ms-access como vínculos a bases de datos de Access almacenadas en bibliotecas de documentos de SharePoint.
  
### <a name="e-6-interoperability-considerations"></a>E-6. Consideraciones de interoperabilidad

Tenga en cuenta que la barra vertical que se usa como delimitador de esta especificación no se encuentra entre los caracteres identificados en la sección 2.2 de RFC 3986 porque está reservado para uso potencial como delimitadores. Esto se hace intencionalmente para maximizar el conjunto de caracteres que el argumento de comando URI puede admitir sin necesidad de codificar los caracteres con porcentaje. Dentro de los segmentos, los caracteres reservados RFC 3986 ":" y "/" forman parte de los datos de argumento, no de delimitadores y, por lo tanto, se incluyen sin \<command-argument\> límite.
  
### <a name="e-7-security-considerations"></a>E-7. Consideraciones de seguridad

En sistemas que tienen controladores registrados para reconocer y actuar en URI ms-access, al hacer clic en un vínculo a un URI ms-access, la aplicación registrada se iniciará, con instrucciones de que la aplicación intente abrir una base de datos en el URI especificado. Las aplicaciones que se registran para procesar URI ms-access deben implementar protecciones para protegerse contra la apertura de bases de datos desde sistemas remotos que no son de confianza y que pueden incluir código malintencionado.
  
### <a name="e-8-references"></a>E-8. Referencias

RFC 3987: Identificadores de recursos internacionales (IRI)  
  
## <a name="appendix-f---uri-scheme-registration-template-for-ms-project-scheme"></a>APÉNDICE F: PLANTILLA DE REGISTRO DE ESQUEMA URI PARA ESQUEMA MS-PROJECT
<a name="bk_addresources"> </a>

### <a name="f-3-uri-scheme-syntax"></a>F-3. Sintaxis de esquema URI

> Esquema de Project = "ms-project:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd
    
> open-for-edit-cmd = "ofe|u|" document-uri
    
> open-for-view-cmd = "ofv|u|" document-uri
    
> new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]
    
> document-uri = ubicación URI de documento para abrir
    
> template-uri = ubicación URI de archivo de plantilla que se usará para el nuevo archivo
    
> save-location\* = ubicación URI de carpeta en la que se creará el nuevo documento
    
> \*save-location es un parámetro opcional
    
### <a name="f-4-uri-scheme-semantics"></a>F-4. Semántica del esquema URI

El esquema ms-project define una sintaxis URI para abrir o crear un documento de Microsoft Project. El esquema define tres comandos que sirven como instrucciones sobre qué se debe hacer con el documento de referencia. Los comandos son 1) open-for-edit-cmd (ofe), que indica a Project que abra el documento en el URI especificado para la edición; 2) open-for-view-cmd (ofv), que indica a Project que abra el documento en el URI especificado en modo de solo lectura; y 3) new-from-template-cmd (nft), que indica a Project que cree un nuevo documento según la plantilla de documento ubicada en el URI template-uri especificado y guarde el nuevo documento en la ubicación especificada en el URI save-location opcional o, si falta el URI opcional, en la ubicación de la biblioteca de documentos predeterminada.
  
### <a name="f-5-applicationsprotocols-that-use-the-ms-project-uri-scheme"></a>F-5. Aplicaciones/protocolos que usan el esquema URI ms-project

Microsoft Office 2013 usa el esquema URI ms-project para invocar Microsoft Project 2013 desde páginas web. Microsoft SharePoint 2013 usa URI ms-project como vínculos a documentos de Project almacenados en bibliotecas de documentos de SharePoint.
  
### <a name="f-6-interoperability-considerations"></a>F-6. Consideraciones de interoperabilidad

Tenga en cuenta que la barra vertical que se usa como delimitador de esta especificación no se encuentra entre los caracteres identificados en la sección 2.2 de RFC 3986 porque está reservado para uso potencial como delimitadores. Esto se hace intencionalmente para maximizar el conjunto de caracteres que el argumento de comando URI puede admitir sin necesidad de codificar los caracteres con porcentaje.
  
Dentro de los segmentos < *argumento-comando*  > los caracteres reservados RFC 3986 ":" y "/" forman parte de los datos del argumento, no los delimitadores y por lo tanto, se incluyen sin secuencias de escape. 
  
### <a name="f-7-security-considerations"></a>F-7. Consideraciones de seguridad

En sistemas que tienen controladores registrados para reconocer y actuar en URI ms-project, al hacer clic en un vínculo a un URI ms-project, la aplicación registrada se iniciará, con instrucciones de que la aplicación intente abrir un documento en el URI especificado. Las aplicaciones que se registran para procesar URI ms-project deben implementar protecciones para protegerse contra la apertura de documentos desde sistemas remotos que no son de confianza y que pueden incluir código malintencionado.
  
### <a name="f-8-references"></a>F-8. Referencias

RFC 3987: Identificadores de recursos internacionales (IRI)  
  
## <a name="appendix-g---uri-scheme-registration-template-for-ms-publisher-scheme"></a>APÉNDICE G: PLANTILLA DE REGISTRO DE ESQUEMA URI PARA ESQUEMA MS-PUBLISHER
<a name="bk_addresources"> </a>

### <a name="g-3-uri-scheme"></a>G-3. Esquema URI

> Sintaxis de esquema de Publisher = "ms-publisher:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd
    
> open-for-edit-cmd = "ofe|u|" document-uri
    
> open-for-view-cmd = "ofv|u|" document-uri
    
> new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]
    
> document-uri = ubicación URI de documento para abrir
    
> template-uri = ubicación URI de archivo de plantilla que se usará para el nuevo archivo
    
> save-location\* = ubicación URI de carpeta en la que se creará el nuevo documento
    
> \*save-location es un parámetro opcional
    
### <a name="g-4-uri-scheme-semantics"></a>G-4. Semántica del esquema URI

El esquema ms-publisher define una sintaxis URI para abrir o crear un documento de Microsoft Publisher. El esquema define tres comandos que sirven como instrucciones sobre qué se debe hacer con el documento de referencia. Los comandos son 1) open-for-edit-cmd (ofe), que indica a Publisher que abra el documento en el URI especificado para la edición; 2) open-for-view-cmd (ofv), que indica a Publisher que abra el documento en el URI especificado en modo de solo lectura; y 3) new-from-template-cmd (nft), que indica a Publisher que cree un nuevo documento según la plantilla de documento ubicada en el URI template-uri especificado y guarde el nuevo documento en la ubicación especificada en el URI save-location opcional o, si falta el URI opcional, en la ubicación de la biblioteca de documentos predeterminada.
  
### <a name="g-5-applicationsprotocols-that-use-the-ms-publisher-uri-scheme"></a>G-5. Aplicaciones/protocolos que usan el esquema URI ms-publisher

Microsoft Office 2013 usa el esquema URI ms-publisher para invocar Microsoft Publisher 2013 o Microsoft Publisher 2010 con Service Pack 2 desde páginas web. Microsoft SharePoint 2013 usa URI ms-publisher como vínculos a documentos de Publisher almacenados en bibliotecas de documentos de SharePoint.
  
### <a name="g-6-interoperability-considerations"></a>G-6. Consideraciones de interoperabilidad

Tenga en cuenta que la barra vertical que se usa como delimitador de esta especificación no se encuentra entre los caracteres identificados en la sección 2.2 de RFC 3986 porque está reservado para uso potencial como delimitadores. Esto se hace intencionalmente para maximizar el conjunto de caracteres que el argumento de comando URI puede admitir sin necesidad de codificar los caracteres con porcentaje. Dentro de los segmentos, los caracteres reservados RFC 3986 ":" y "/" forman parte de los datos del argumento, no de delimitadores y, por lo tanto, se incluyen sin \<command-argument\> delimitar.
  
### <a name="g-7-security-considerations"></a>G-7. Consideraciones de seguridad

En sistemas que tienen controladores registrados para reconocer y actuar en URI ms-publisher, al hacer clic en un vínculo a un URI ms-publisher, la aplicación registrada se iniciará, con instrucciones de que la aplicación intente abrir un documento en el URI especificado. Las aplicaciones que se registran para procesar URI ms-publisher deben implementar protecciones para protegerse contra la apertura de documentos desde sistemas remotos que no son de confianza y que pueden incluir código malintencionado.
  
### <a name="g-9-references"></a>G-9. Referencias

RFC 3987: Identificadores de recursos internacionales (IRI)  
  
## <a name="appendix-h---uri-scheme-registration-template-for-ms-spd-scheme"></a>APÉNDICE H: PLANTILLA DE REGISTRO DE ESQUEMA URI PARA ESQUEMA MS-SPD
<a name="bk_addresources"> </a>

### <a name="h-3-uri-scheme-syntax"></a>H-3. Sintaxis de esquema URI

> Esquema de SharePoint Designer = "ms-spd:" open-for-edit-cmd
    
> open-for-edit-cmd = "ofe|u|" document-uri
    
> document-uri = ubicación URI de documento para abrir
    
### <a name="h-4-uri-scheme-semantics"></a>H-4. Semántica de esquema URI

El esquema ms-spd define una sintaxis URI para abrir un documento de Microsoft SharePoint Designer. El esquema define dos comandos que sirven como instrucciones sobre qué se debe hacer con el documento de referencia. Los comandos son 1) open-for-edit-cmd (ofe), que indica a SharePoint Designer que abra el documento en el URI especificado para la edición; y 2) open-for-view-cmd (ofv), que indica a SharePoint Designer que abra el documento en el URI especificado en modo de solo lectura.
  
### <a name="h-5-applicationsprotocols-that-use-the-ms-spd-uri-scheme"></a>H-5. Aplicaciones/protocolos que usan el esquema URI ms-spd

Microsoft Office 2013 usa el esquema URI ms-spd para invocar Microsoft SharePoint Designer 2013 desde páginas web. Microsoft SharePoint 2013 usa URI ms-spd como vínculos a documentos de SharePoint Designer almacenados en bibliotecas de documentos de SharePoint.
  
### <a name="h-6-interoperability-considerations"></a>H-6. Consideraciones de interoperabilidad

Tenga en cuenta que la barra vertical que se usa como delimitador de esta especificación no se encuentra entre los caracteres identificados en la sección 2.2 de RFC 3986 porque está reservado para uso potencial como delimitadores. Esto se hace intencionalmente para maximizar el conjunto de caracteres que el argumento de comando URI puede admitir sin necesidad de codificar los caracteres con porcentaje.
  
Dentro de los segmentos < *argumento-comando*  > los caracteres reservados RFC 3986 ":" y "/" forman parte de los datos del argumento, no los delimitadores y por lo tanto, se incluyen sin secuencias de escape. 
  
### <a name="h-7-security-considerations"></a>H-7. Consideraciones de seguridad

En sistemas que tienen controladores registrados para reconocer y actuar en URI ms-spd, al hacer clic en un vínculo a un URI ms-spd, la aplicación registrada se iniciará, con instrucciones de que la aplicación intente abrir un documento en el URI especificado. Las aplicaciones que se registran para procesar URI ms-spd deben implementar protecciones para protegerse contra la apertura de documentos desde sistemas remotos que no son de confianza y que pueden incluir código malintencionado.
  
### <a name="h-8-references"></a>H-8. Referencias

RFC 3987: Identificadores de recursos internacionales (IRI)  
  
## <a name="appendix-i---uri-scheme-registration-template-for-ms-infopath-scheme"></a>APÉNDICE I: PLANTILLA DE REGISTRO DE ESQUEMA URI PARA ESQUEMA MS-INFOPATH
<a name="bk_addresources"> </a>

###   <a name="i-3-uri-scheme-syntax"></a>I-3. Sintaxis de esquema URI

> Esquema de Infopath = "ms-infopath:" open-for-edit-cmd | open-for-view-cmd
    
> open-for-edit-cmd = "ofe|u|" document-uri
    
> open-for-view-cmd = "ofv|u|" document-uri
    
> document-uri = ubicación URI de documento para abrir
    
### <a name="i-4-uri-scheme-semantics"></a>I-4. Semántica de esquema URI

El esquema ms-infopath define una sintaxis URI para abrir o crear un documento de Microsoft Infopath. El esquema define dos comandos que sirven como instrucciones sobre qué se debe hacer con el documento de referencia. Los comandos son 1) open-for-edit-cmd (ofe), que indica a InfoPath que abra el documento en el URI especificado para su edición; y 2) open-for-view-cmd (ofv), que indica a InfoPath que abra el documento en el URI especificado en modo de solo lectura.
  
### <a name="i-5-applicationsprotocols-that-use-the-ms-infopath-uri-scheme"></a>I-5. Aplicaciones/protocolos que usan el esquema URI ms-infopath

Microsoft Office 2013 usa el esquema URI ms-infopath para invocar Microsoft Infopath 2013 desde páginas web. Microsoft SharePoint 2013 usa URI ms-infopath como vínculos a documentos de Infopath almacenados en bibliotecas de documentos de SharePoint.
  
### <a name="i-6-interoperability-considerations"></a>I-6. Consideraciones de interoperabilidad

Tenga en cuenta que la barra vertical que se usa como delimitador de esta especificación no se encuentra entre los caracteres identificados en la sección 2.2 de RFC 3986 porque está reservado para uso potencial como delimitadores. Esto se hace intencionalmente para maximizar el conjunto de caracteres que el argumento de comando URI puede admitir sin necesidad de codificar los caracteres con porcentaje.
  
Dentro de los segmentos < *argumento-comando*  > los caracteres reservados RFC 3986 ":" y "/" forman parte de los datos del argumento, no los delimitadores y por lo tanto, se incluyen sin secuencias de escape. 
  
### <a name="i-7-security-considerations"></a>I-7. Consideraciones de seguridad

En sistemas que tienen controladores registrados para reconocer y actuar en URI ms-infopath, al hacer clic en un vínculo a un URI ms-infopath, la aplicación registrada se iniciará, con instrucciones de que la aplicación intente abrir un documento en el URI especificado. Las aplicaciones que se registran para procesar URI ms-infopath deben implementar protecciones para protegerse contra la apertura de documentos desde sistemas remotos que no son de confianza y que pueden incluir código malintencionado.
  
### <a name="i-8-references"></a>I-8. Referencias

RFC 3987: Identificadores de recursos internacionales (IRI)  
  
