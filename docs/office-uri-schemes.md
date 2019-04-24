---
title: Esquemas URI de Office
manager: luken
ms.date: 01/14/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1ea99a8f-b005-4b92-b313-923294d20fbf
ms.openlocfilehash: 71325af974e4778d65bea7d74561bde3c9c8bca2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299716"
---
# <a name="office-uri-schemes"></a><span data-ttu-id="5ef95-102">Esquemas URI de Office</span><span class="sxs-lookup"><span data-stu-id="5ef95-102">Office URI Schemes</span></span>

## <a name="11-abstract"></a><span data-ttu-id="5ef95-103">1.1 RESUMEN</span><span class="sxs-lookup"><span data-stu-id="5ef95-103">1.1 ABSTRACT</span></span>

<span data-ttu-id="5ef95-p101">Este documento define el formato de los identificadores uniformes de recursos (URI) para las aplicaciones de productividad de Office. Se admite el esquema en el Service Pack 2 de Microsoft Office 2010 y versiones posteriores, incluidos Microsoft Office 2013 para Windows y los productos de Microsoft SharePoint 2013. También se admite en Office para iPhone, Office para iPad y Office para Mac 2011.</span><span class="sxs-lookup"><span data-stu-id="5ef95-p101">This document defines the format of Uniform Resource Identifiers (URIs) for office productivity applications. The scheme is supported in Microsoft Office 2010 Service Pack 2 and later, including the Microsoft Office 2013 for Windows and the Microsoft SharePoint 2013 products. It is also supported in Office for iPhone, Office for iPad, and Office for Mac 2011.</span></span>
  
## <a name="12-introduction"></a><span data-ttu-id="5ef95-107">1.2 INTRODUCCIÓN</span><span class="sxs-lookup"><span data-stu-id="5ef95-107">1.2 INTRODUCTION</span></span>

<span data-ttu-id="5ef95-p102">Estos esquemas URI permiten invocar con diversos comandos las aplicaciones de productividad de Office. Cada aplicación recibe un esquema con nombre diferente, pero todos los esquemas siguen las mismas reglas para la formación de URI (esquema URI).</span><span class="sxs-lookup"><span data-stu-id="5ef95-p102">These URI schemes allow for office productivity applications to be invoked with various commands. Each application is given a different named scheme but all schemes follow the same rules for how the URI is formed (URI Schema).</span></span>
  
## <a name="13-uri-schema"></a><span data-ttu-id="5ef95-110">1.3 ESQUEMA URI</span><span class="sxs-lookup"><span data-stu-id="5ef95-110">1.3 URI SCHEMA</span></span>

### <a name="full-schema"></a><span data-ttu-id="5ef95-111">Esquema completo</span><span class="sxs-lookup"><span data-stu-id="5ef95-111">Full schema</span></span>

<span data-ttu-id="5ef95-112">< *nombre-esquema*  >:<  *nombre-comando*  >"|"<  *descriptor-argumento-comando*  > "|"<  *argumento-comando*  ></span><span class="sxs-lookup"><span data-stu-id="5ef95-112">< *scheme-name*  >:<  *command-name*  >"|"<  *command-argument-descriptor*  > "|"<  *command-argument*  ></span></span> 
  
<span data-ttu-id="5ef95-p103">Un URI, tal y como se define en este documento puede tener un argumento de comando o más, cada uno de los cuales debe incluir los elementos < *descriptor-argumento-comando*  > y el <  *argumento-comando*  > y debe estar delimitado con el carácter de barra vertical ("|"). Cuando se incluye un argumento de comando o más en un URI, debe haber un carácter de barra vertical ("|") para separar cada argumento de comando del argumento de comando siguiente.</span><span class="sxs-lookup"><span data-stu-id="5ef95-p103">A URI as defined in this document may have one or more command arguments, each of which must include both the < *command-argument-descriptor*  > and the <  *command-argument*  > elements and be delimited by the vertical bar ("|") character. When more than one command argument is included in a URI there must be a vertical bar ("|") character separating each command argument from the following command argument.</span></span> 
  
<span data-ttu-id="5ef95-p104">Estos esquemas no incluyen un componente de la entidad emisora tal como se define en la sección 3.2 de RFC 3986. La invocación de los comandos especificados en este documento se realiza en el contexto del sistema al invocar el comando. Por ejemplo, cuando se invoca el URI "ms-excel:ofv|u|https://contoso/Q4/budget.xls" desde un equipo que tiene Microsoft Windows con Microsoft Office 2013 instalado, el resultado que se espera es que se ejecutará la instalación local de Microsoft Excel y se pasarán argumentos para abrir el archivo en  *https://contoso/Q4/budget.xls*  en modo de solo lectura. Tenga en cuenta que la barra vertical que se usa como delimitador de esta especificación no se encuentra entre los caracteres identificados en la sección 2.2 de RFC 3986 porque está reservado para uso potencial como delimitadores. Esto se hace intencionalmente para maximizar el conjunto de caracteres que el argumento de comando URI puede admitir sin necesidad de codificar los caracteres con porcentaje.</span><span class="sxs-lookup"><span data-stu-id="5ef95-p104">These schemes do not include an authority component as defined in section 3.2 of RFC 3986. Invocation of the commands specified in this document takes place in the context of the system invoking the command. For example, when the URI "ms-excel:ofv|u|https://contoso/Q4/budget.xls" is invoked from a personal computer running Microsoft Windows with Microsoft Office 2013 installed the expected result is that the local installation of Microsoft Excel will be launched and passed arguments to open the file at  *https://contoso/Q4/budget.xls*  in read-only mode. Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters. This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters.</span></span> 
  
<span data-ttu-id="5ef95-120">La sintaxis de esquema incluye lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="5ef95-120">The scheme syntax includes the following:</span></span>
  
1. <span data-ttu-id="5ef95-p105">< *nombre-esquema*  >: Hace referencia al tipo de aplicación que se debe invocar. Por ejemplo, el nombre del esquema ms-word se registra con Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="5ef95-p105">< *scheme-name*  >: This refers to the type of application that should be invoked. For instance, the ms-word: scheme name is registered by Microsoft Word.</span></span> 
    
2. <span data-ttu-id="5ef95-123">Separador ":"</span><span class="sxs-lookup"><span data-stu-id="5ef95-123">":" separator</span></span>
    
3. <span data-ttu-id="5ef95-p106">< *nombre-comando*  >: Describe las acciones que debe realizar la aplicación. Por ejemplo, abrir un documento para su visualización. La lista de nombres de comando se describe en la sección 1.5.</span><span class="sxs-lookup"><span data-stu-id="5ef95-p106">< *command-name*  >: This describes the actions that the application should perform. For instance, opening a document for viewing. The list of command names is described in section 1.5.</span></span> 
    
4. <span data-ttu-id="5ef95-127">Separador "|" (barra vertical)</span><span class="sxs-lookup"><span data-stu-id="5ef95-127">"|" (vertical bar) separator</span></span>
    
5. <span data-ttu-id="5ef95-128">< *descriptor-argumento-comando*  >: Este elemento proporciona más información sobre el argumento del comando.</span><span class="sxs-lookup"><span data-stu-id="5ef95-128">< *command-argument-descriptor*  >: This element gives more information about what the command argument is about.</span></span> 
    
6. <span data-ttu-id="5ef95-129">Separador "|" (barra vertical)</span><span class="sxs-lookup"><span data-stu-id="5ef95-129">"|" (vertical bar) separator</span></span>
    
7. <span data-ttu-id="5ef95-p107">< *argumento-comando*  >: Los argumentos varían según el comando. Un argumento común es el URI para un documento, normalmente mediante el esquema http o https. Tenga en cuenta que dentro de los segmentos <  *argumento-comando*  > los caracteres reservados RFC 3986 ":" y "/" forman parte de los datos del argumento, no los delimitadores y por lo tanto, se incluyen sin secuencias de escape.</span><span class="sxs-lookup"><span data-stu-id="5ef95-p107">< *command-argument*  >: The arguments vary depending on the command. One common argument is the URI to a document, typically using the http or https scheme. Note that within <  *command-argument*  > segments the RFC 3986 reserved characters ":" and "/" are part of the argument data, not delimiters, and are therefore included unescaped.</span></span> 
    
### <a name="abbreviated-schema"></a><span data-ttu-id="5ef95-133">Esquema abreviado</span><span class="sxs-lookup"><span data-stu-id="5ef95-133">Abbreviated schema</span></span>

<span data-ttu-id="5ef95-p108">An abbreviated form of the office URI schemes allows for a more compact request to launch a specified Office application to open the resource located at a given URI. This abbreviated form implies the < *command-name*  > "ofv" and the <  *command-argument-descriptor*  > "u". No further commands or command arguments are allowed in this schema.</span><span class="sxs-lookup"><span data-stu-id="5ef95-p108">An abbreviated form of the office URI schemes allows for a more compact request to launch a specified Office application to open the resource located at a given URI. This abbreviated form implies the < *command-name*  > "ofv" and the <  *command-argument-descriptor*  > "u". No further commands or command arguments are allowed in this schema.</span></span> 
  
<span data-ttu-id="5ef95-137">< *nombre-esquema*  >:<  *argumento-comando*  ></span><span class="sxs-lookup"><span data-stu-id="5ef95-137">< *scheme-name*  >:<  *command-argument*  ></span></span> 
  
1. <span data-ttu-id="5ef95-p109">< *nombre-esquema*  >: El tipo de aplicación que se debe invocar. Por ejemplo, ms-word: para Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="5ef95-p109">< *scheme-name*  >: the type of application that should be invoked. For instance ms-word: for Microsoft Word.</span></span> 
    
2. <span data-ttu-id="5ef95-p110">< *argumento-comando*  >: URI para el recurso que la aplicación debe abrir. Se admiten URI únicos basados en esquemas http o https.</span><span class="sxs-lookup"><span data-stu-id="5ef95-p110">< *command-argument*  >: URI for the resource the application should open. Currently only URIs based on the http or https scheme are supported.</span></span> 
    
## <a name="14-scheme-names-and-office-application-registrations"></a><span data-ttu-id="5ef95-142">1.4 NOMBRES DE ESQUEMAS Y REGISTROS DE APLICACIONES DE OFFICE</span><span class="sxs-lookup"><span data-stu-id="5ef95-142">1.4 SCHEME NAMES AND OFFICE APPLICATION REGISTRATIONS</span></span>

<span data-ttu-id="5ef95-p111">La siguiente es la lista de nombres de esquemas implementados en aplicaciones de Microsoft Office. Cuando se instala Microsoft Office, se registra cada nombre del esquema con Windows para ser controlado por el producto de Office del mismo nombre. Tenga en cuenta que "ms-spd" es una abreviatura de SharePoint Designer.</span><span class="sxs-lookup"><span data-stu-id="5ef95-p111">The following is the list of scheme names implemented in Microsoft Office applications. When Microsoft Office is installed, each scheme name is registered with Windows to be handled by the Office product of the same name. Note that "ms-spd" is an abbreviation for SharePoint Designer.</span></span>
  
> - <span data-ttu-id="5ef95-146">*ms-word:*</span><span class="sxs-lookup"><span data-stu-id="5ef95-146">*ms-word:*</span></span> 
    
> - <span data-ttu-id="5ef95-147">*ms-powerpoint:*</span><span class="sxs-lookup"><span data-stu-id="5ef95-147">*ms-powerpoint:*</span></span> 
    
> - <span data-ttu-id="5ef95-148">*ms-excel:*</span><span class="sxs-lookup"><span data-stu-id="5ef95-148">*ms-excel:*</span></span> 
    
> - <span data-ttu-id="5ef95-149">*ms-visio:*</span><span class="sxs-lookup"><span data-stu-id="5ef95-149">*ms-visio:*</span></span> 
    
> - <span data-ttu-id="5ef95-150">*ms-access:*</span><span class="sxs-lookup"><span data-stu-id="5ef95-150">*ms-access:*</span></span> 
    
> - <span data-ttu-id="5ef95-151">*ms-project:*</span><span class="sxs-lookup"><span data-stu-id="5ef95-151">*ms-project:*</span></span> 
    
> - <span data-ttu-id="5ef95-152">*ms-publisher:*</span><span class="sxs-lookup"><span data-stu-id="5ef95-152">*ms-publisher:*</span></span> 
    
> - <span data-ttu-id="5ef95-153">*ms-spd:*</span><span class="sxs-lookup"><span data-stu-id="5ef95-153">*ms-spd:*</span></span> 
    
> - <span data-ttu-id="5ef95-154">*ms-infopath:*</span><span class="sxs-lookup"><span data-stu-id="5ef95-154">*ms-infopath:*</span></span> 
    
## <a name="15-commands-and-required-command-arguments"></a><span data-ttu-id="5ef95-155">1.5 COMANDOS Y ARGUMENTOS DE COMANDO NECESARIOS</span><span class="sxs-lookup"><span data-stu-id="5ef95-155">1.5 COMMANDS AND REQUIRED COMMAND ARGUMENTS</span></span>

### <a name="view-document"></a><span data-ttu-id="5ef95-156">Ver documento</span><span class="sxs-lookup"><span data-stu-id="5ef95-156">View Document</span></span>

<span data-ttu-id="5ef95-157">El siguiente comando hará que la aplicación abra el documento al que hace referencia el URI en modo de solo lectura o vista.</span><span class="sxs-lookup"><span data-stu-id="5ef95-157">The following command will cause the application to open the document referenced by the URI in a read-only or view mode.</span></span>
  
> <span data-ttu-id="5ef95-158">Nombre del comando: ofv</span><span class="sxs-lookup"><span data-stu-id="5ef95-158">Command Name: ofv</span></span>
    
> <span data-ttu-id="5ef95-159">Descriptor de argumento de comando: u</span><span class="sxs-lookup"><span data-stu-id="5ef95-159">Command argument descriptor: u</span></span>
    
> <span data-ttu-id="5ef95-160">Argumento de comando: Un URI para el documento, según el esquema http o https</span><span class="sxs-lookup"><span data-stu-id="5ef95-160">Command argument: a URI to the document, based on the http or https scheme</span></span>
    
> <span data-ttu-id="5ef95-161">Ejemplo:  *ms-excel:ofv|u|https://contoso/Q4/budget.xls*</span><span class="sxs-lookup"><span data-stu-id="5ef95-161">Example:  *ms-excel:ofv|u|https://contoso/Q4/budget.xls*</span></span> 
    
### <a name="edit-document"></a><span data-ttu-id="5ef95-162">Editar documento</span><span class="sxs-lookup"><span data-stu-id="5ef95-162">Edit Document</span></span>

<span data-ttu-id="5ef95-163">El siguiente comando hará que la aplicación abra el documento al que hace referencia el URI en modo de edición</span><span class="sxs-lookup"><span data-stu-id="5ef95-163">The following command will cause the application to open the document referenced by the URI in editing mode.</span></span>
  
> <span data-ttu-id="5ef95-164">Nombre del comando: ofe</span><span class="sxs-lookup"><span data-stu-id="5ef95-164">Command Name: ofe</span></span>
    
> <span data-ttu-id="5ef95-165">Descriptor de argumento de comando: u</span><span class="sxs-lookup"><span data-stu-id="5ef95-165">Command argument descriptor: u</span></span>
    
> <span data-ttu-id="5ef95-166">Argumento de comando: Un URI para el documento, según el esquema http o https</span><span class="sxs-lookup"><span data-stu-id="5ef95-166">Command argument: a URI to the document, based on the http or https scheme</span></span>
    
> <span data-ttu-id="5ef95-167">Ejemplo:  *ms-powerpoint:ofe|u|https://www.fourthcoffee.com/AllHandsDeck.ppt*</span><span class="sxs-lookup"><span data-stu-id="5ef95-167">Example:  *ms-powerpoint:ofe|u|https://www.fourthcoffee.com/AllHandsDeck.ppt*</span></span> 
    
### <a name="new-document-from-template"></a><span data-ttu-id="5ef95-168">Nuevo documento de plantilla</span><span class="sxs-lookup"><span data-stu-id="5ef95-168">New Document from Template</span></span>

<span data-ttu-id="5ef95-p112">El siguiente comando hará que la aplicación cree y abra un nuevo documento según la plantilla almacenada en el URI especificado. No se modifica el archivo de plantilla en este proceso. Puede proporcionarse un argumento de comando adicional para especificar la ruta predeterminada ofrecida como ubicación de guardado cuando se guarda el archivo por primera vez. Es posible que el usuario elija una ubicación diferente.</span><span class="sxs-lookup"><span data-stu-id="5ef95-p112">The following command will cause the application to create and open a new document based on the template stored at the specified URI. The template file is not modified in this process. An additional command argument may be supplied to specify the default path offered as a save location when the file is first saved. It is possible for the user to choose a different location.</span></span>
  
> <span data-ttu-id="5ef95-173">Nombre del comando: nft</span><span class="sxs-lookup"><span data-stu-id="5ef95-173">Command Name: nft</span></span>
    
> <span data-ttu-id="5ef95-174">Descriptor de argumento de comando 1: u</span><span class="sxs-lookup"><span data-stu-id="5ef95-174">Command argument descriptor 1: u</span></span>
    
> <span data-ttu-id="5ef95-175">Argumento de comando 1: Un URI para la plantilla, según el esquema http o https</span><span class="sxs-lookup"><span data-stu-id="5ef95-175">Command argument 1: a URI to the template, based on the http or https scheme</span></span>
    
> <span data-ttu-id="5ef95-176">Descriptor de argumento de comando opcional 2: s</span><span class="sxs-lookup"><span data-stu-id="5ef95-176">Optional Command argument descriptor 2: s</span></span>
    
> <span data-ttu-id="5ef95-177">Argumento de comando opcional 2: URI para especificar la carpeta de guardado predeterminada</span><span class="sxs-lookup"><span data-stu-id="5ef95-177">Optional Command argument 2: URI to specify the default save folder</span></span>
    
> <span data-ttu-id="5ef95-178">Ejemplo:  *ms-word:nft|u|https://cohowinery/templates/elegance.pot|s|https://cohowinery/presentations*</span><span class="sxs-lookup"><span data-stu-id="5ef95-178">Example:  *ms-word:nft|u|https://cohowinery/templates/elegance.pot|s|https://cohowinery/presentations*</span></span> 
    
<span data-ttu-id="5ef95-179">Como nota, si se proporciona la ubicación de guardado predeterminada opcional, debe estar apuntando al mismo nombre de host que la plantilla.</span><span class="sxs-lookup"><span data-stu-id="5ef95-179">As a note, if the optional default save location is supplied, it must be pointing to the same host name as the template.</span></span>
  
<span data-ttu-id="5ef95-180">Además, las aplicaciones de SharePoint Designer e InfoPath (que implementan el esquema ms-spd: y los esquemas ms-infopath:, respectivamente) no admiten la funcionalidad "nuevo documento de plantilla".</span><span class="sxs-lookup"><span data-stu-id="5ef95-180">Additionally, the SharePoint Designer and InfoPath applications (which implement the ms-spd: scheme and ms-infopath: schemes, respectively) do not support the "new document from template" functionality.</span></span>
  
## <a name="16-backwards-compatibility"></a><span data-ttu-id="5ef95-181">1.6 COMPATIBILIDAD CON VERSIONES ANTERIORES</span><span class="sxs-lookup"><span data-stu-id="5ef95-181">1.6 BACKWARDS COMPATIBILITY</span></span>

<span data-ttu-id="5ef95-p113">Al analizar un URI para extraer los argumentos de comando adecuados para un comando determinado, el controlador URI de Office solo usará los argumentos de comando que tengan el descriptor de argumento de comando esperado. Si hay pares adicionales de argumentos y descriptores de argumentos que tengan descriptores de argumento inesperados, se quitarán del URI. Este mecanismo permite que las versiones futuras del esquema agreguen argumentos de comando adicionales sin interrumpir la compatibilidad con implementaciones heredadas de este esquema.</span><span class="sxs-lookup"><span data-stu-id="5ef95-p113">When parsing a URI to extract the appropriate command arguments for a given command, the Office URI handler will only use the command arguments that have the expected command argument descriptor. If there are additional pairs of arguments and argument descriptors that have unexpected argument descriptors, they will be removed from the URI. This mechanism allows future versions of the scheme to add additional command arguments without breaking backward compatibility with legacy implementations of this scheme.</span></span>
  
## <a name="17-implementation-restrictions-on-command-arguments"></a><span data-ttu-id="5ef95-185">1.7 RESTRICCIONES DE IMPLEMENTACIÓN EN ARGUMENTOS DE COMANDO</span><span class="sxs-lookup"><span data-stu-id="5ef95-185">1.7 IMPLEMENTATION RESTRICTIONS ON COMMAND ARGUMENTS</span></span>

<span data-ttu-id="5ef95-186">Se colocan las siguientes restricciones en argumentos de comando en su implementación actual de Office 2013.</span><span class="sxs-lookup"><span data-stu-id="5ef95-186">The below restrictions are placed on command arguments in its current implementation in Office 2013.</span></span>
  
### <a name="length-limitations-on-uri-command-arguments"></a><span data-ttu-id="5ef95-187">Limitaciones de longitud en argumentos de comando URI</span><span class="sxs-lookup"><span data-stu-id="5ef95-187">Length limitations on URI command arguments</span></span>

<span data-ttu-id="5ef95-p114">Para argumentos de comando URI, la longitud de ruta máxima es de 256 caracteres para todas las aplicaciones excepto Excel, donde el límite es de 216. Se pueden admitir longitudes de ruta mayores que estas según cada aplicación individual, y se recomienda realizar una prueba antes de implementar las soluciones que dependen de esto.</span><span class="sxs-lookup"><span data-stu-id="5ef95-p114">For URI command arguments, the maximum path length is 256 characters for all apps except Excel, where the limit is 216. Path lengths greater than these may be supported on an app-by-app basis and testing is recommended before deploying any solutions that rely on this.</span></span>
  
### <a name="allowed-characters-in-uri-command-arguments"></a><span data-ttu-id="5ef95-190">Caracteres permitidos en argumentos de comando URI</span><span class="sxs-lookup"><span data-stu-id="5ef95-190">Allowed characters in URI command arguments</span></span>

<span data-ttu-id="5ef95-p115">Los URI permitidos deben cumplir con los estándares propuestos en RFC 3987: Identificadores de recursos internacionalizados (IRI). Los caracteres identificados como reservados en RFC 3986 no deben estar cifrados con porcentaje. Los nombres de archivo no deben contener ninguno de los siguientes caracteres: \ / : ? \< \> | " o \*.</span><span class="sxs-lookup"><span data-stu-id="5ef95-p115">Allowed URIs must conform to the standards proposed in RFC 3987 - Internationalized Resource Identifiers (IRIs) . Characters identified as reserved in RFC 3986 should not be percent encoded. . Filenames must not contain any of the following characters: \ / : ? \< \> | " or \*.</span></span>  
  
## <a name="appendix-a---uri-scheme-registration-template-for-ms-word-scheme"></a><span data-ttu-id="5ef95-196">APÉNDICE A: PLANTILLA DE REGISTRO DE ESQUEMA URI PARA ESQUEMA MS-WORD</span><span class="sxs-lookup"><span data-stu-id="5ef95-196">APPENDIX A - URI SCHEME REGISTRATION TEMPLATE FOR MS-WORD SCHEME</span></span>
<span data-ttu-id="5ef95-197"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="5ef95-197"></span></span>

### <a name="a-3-uri-scheme-syntax"></a><span data-ttu-id="5ef95-p116">A-3. Sintaxis de esquema URI</span><span class="sxs-lookup"><span data-stu-id="5ef95-p116">A-3. URI Scheme Syntax</span></span>

> <span data-ttu-id="5ef95-200">Esquema de Word = "ms-word:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span><span class="sxs-lookup"><span data-stu-id="5ef95-200">Word Scheme = "ms-word:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span></span>
    
> <span data-ttu-id="5ef95-201">open-for-edit-cmd = "ofe|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="5ef95-201">open-for-edit-cmd = "ofe|u|" document-uri</span></span>
    
> <span data-ttu-id="5ef95-202">open-for-view-cmd = "ofv|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="5ef95-202">open-for-view-cmd = "ofv|u|" document-uri</span></span>
    
> <span data-ttu-id="5ef95-203">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span><span class="sxs-lookup"><span data-stu-id="5ef95-203">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span></span>
    
> <span data-ttu-id="5ef95-204">document-uri = ubicación URI de documento para abrir</span><span class="sxs-lookup"><span data-stu-id="5ef95-204">document-uri = URI location of document to open</span></span>
    
> <span data-ttu-id="5ef95-205">template-uri = ubicación URI de archivo de plantilla que se usará para el nuevo archivo</span><span class="sxs-lookup"><span data-stu-id="5ef95-205">template-uri = URI location of template file upon which new file will be based</span></span>
    
> <span data-ttu-id="5ef95-206">save-location = ubicación URI de carpeta en la que se creará el nuevo documento</span><span class="sxs-lookup"><span data-stu-id="5ef95-206">save-location = URI location of folder in which new document should be created</span></span>
    
### <a name="a-4-uri-scheme-semantics"></a><span data-ttu-id="5ef95-p117">A-4. Semántica de esquema URI</span><span class="sxs-lookup"><span data-stu-id="5ef95-p117">A-4. URI Scheme Semantics</span></span>

<span data-ttu-id="5ef95-p118">El esquema ms-word define una sintaxis URI para abrir o crear un documento de procesador de texto. El esquema define tres comandos que sirven como instrucciones sobre qué se debe hacer con el documento de referencia. Los comandos son 1) open-for-edit-cmd (ofe), que indica a un procesador de texto que abra el documento en el URI especificado para la edición; 2) open-for-view-cmd (ofv), que indica a un procesador de texto que abra el documento en el URI especificado en modo de solo lectura; y 3) new-from-template-cmd (nft), que indica a un procesador de texto que cree un nuevo documento según la plantilla de documento ubicada en el URI template-uri especificado y guarde el nuevo documento en la ubicación especificada en el URI save-location opcional o, si falta el URI opcional, en la ubicación de la biblioteca de documentos predeterminada.</span><span class="sxs-lookup"><span data-stu-id="5ef95-p118">The ms-word scheme defines a URI syntax for opening or creating a word processing document. The scheme defines three commands that serve as instructions regarding what should be done with the referenced document. The commands are 1) open-for-edit-cmd (ofe), which instructs a word processing application to open the document at the specified URI for editing; 2) open-for-view-cmd (ofv), which instructs a word processing application to open the document at the specified URI in a read-only mode; and 3) new-from-template-cmd (nft), which instructs a word processing application to create a new document based on the document template located at the specified template-uri URI and save the new document either in the location specified in the optional save-location URI or, in the absence of that optional URI, in the default document library location.</span></span>
  
### <a name="a-5-applicationsprotocols-that-use-the-ms-word-uri-scheme"></a><span data-ttu-id="5ef95-p119">A-5. Aplicaciones/protocolos que usan el esquema URI ms-word</span><span class="sxs-lookup"><span data-stu-id="5ef95-p119">A-5. Applications/Protocols that use the ms-word URI Scheme</span></span>

<span data-ttu-id="5ef95-p120">Microsoft Office 2013 usa el esquema URI ms-word para invocar Microsoft Word 2013 o Microsoft Word 2010 con Service Pack 2. Microsoft SharePoint 2013 usa URI ms-word como vínculos a documentos de procesador de texto almacenados en bibliotecas de documentos de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="5ef95-p120">The ms-word URI Scheme is used by Microsoft Office 2013 to invoke Microsoft Word 2013 or Microsoft Word 2010 with Service Pack 2. Microsoft SharePoint 2013 uses ms-word URIs as links to word processing documents stored in SharePoint document libraries.</span></span>
  
### <a name="a-6-interoperability-considerations"></a><span data-ttu-id="5ef95-p121">A-6. Consideraciones de interoperabilidad</span><span class="sxs-lookup"><span data-stu-id="5ef95-p121">A-6. Interoperability Considerations</span></span>

<span data-ttu-id="5ef95-p122">Tenga en cuenta que la barra vertical que se usa como delimitador de esta especificación no se encuentra entre los caracteres identificados en la sección 2.2 de RFC 3986 porque está reservado para uso potencial como delimitadores. Esto se hace intencionalmente para maximizar el conjunto de caracteres que el argumento de comando URI puede admitir sin necesidad de codificar los caracteres con porcentaje.</span><span class="sxs-lookup"><span data-stu-id="5ef95-p122">Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters.. This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters.</span></span>
  
<span data-ttu-id="5ef95-220">Dentro de los segmentos < *argumento-comando*  > los caracteres reservados RFC 3986 ":" y "/" forman parte de los datos del argumento, no los delimitadores y por lo tanto, se incluyen sin secuencias de escape.</span><span class="sxs-lookup"><span data-stu-id="5ef95-220">Within < *command-argument*  > segments the RFC 3986 reserved characters ":" and "/" are part of the argument data, not delimiters, and are therefore included unescaped.</span></span> 
  
### <a name="a-7-security-considerations"></a><span data-ttu-id="5ef95-p123">A-7. Consideraciones de seguridad</span><span class="sxs-lookup"><span data-stu-id="5ef95-p123">A-7. Security Considerations</span></span>

 <span data-ttu-id="5ef95-p124">En sistemas que tienen controladores registrados para reconocer y actuar en URI ms-word, al hacer clic en un vínculo a un URI ms-word, el procesador de texto registrado se iniciará, con instrucciones de que el procesador de texto intente abrir un documento en el URI especificado. Los procesadores de texto que se registran para procesar URI ms-word deben implementar protecciones para protegerse contra la apertura de documentos desde sistemas remotos que no son de confianza y que pueden incluir código malintencionado.</span><span class="sxs-lookup"><span data-stu-id="5ef95-p124">On systems that have registered handlers to recognize and act on ms-word URIs, clicking on a link to an ms-word URI will cause the registered word processing application to be launched, with instructions to the word processing application to attempt to open a document at the specified URI. Word processing applications registering to process ms-word URIs should implement protections to guard against opening documents from untrusted remote systems that may include malicious code.</span></span> 
  
### <a name="a-8-references"></a><span data-ttu-id="5ef95-p125">A-8. Referencias</span><span class="sxs-lookup"><span data-stu-id="5ef95-p125">A-8. References</span></span>

<span data-ttu-id="5ef95-227">RFC 3987: Identificadores de recursos internacionales (IRI)</span><span class="sxs-lookup"><span data-stu-id="5ef95-227">RFC 3987 - International Resource Identifiers (IRIs)</span></span>  
  
## <a name="appendix-b---uri-scheme-registration-template-for-ms-powerpoint-scheme"></a><span data-ttu-id="5ef95-228">APÉNDICE B: PLANTILLA DE REGISTRO DE ESQUEMA URI PARA ESQUEMA MS-POWERPOINT</span><span class="sxs-lookup"><span data-stu-id="5ef95-228">APPENDIX B - URI SCHEME REGISTRATION TEMPLATE FOR MS-POWERPOINT SCHEME</span></span>
<span data-ttu-id="5ef95-229"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="5ef95-229"></span></span>

### <a name="b-3-uri-scheme-syntax"></a><span data-ttu-id="5ef95-p126">B-3. Sintaxis de esquema URI</span><span class="sxs-lookup"><span data-stu-id="5ef95-p126">B-3. URI Scheme Syntax</span></span>

- <span data-ttu-id="5ef95-232">Esquema de PowerPoint = "ms-powerpoint:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span><span class="sxs-lookup"><span data-stu-id="5ef95-232">PowerPoint Scheme = "ms-powerpoint:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span></span>
    
- <span data-ttu-id="5ef95-233">open-for-edit-cmd = "ofe|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="5ef95-233">open-for-edit-cmd = "ofe|u|" document-uri</span></span>
    
- <span data-ttu-id="5ef95-234">open-for-view-cmd = "ofv|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="5ef95-234">open-for-view-cmd = "ofv|u|" document-uri</span></span>
    
- <span data-ttu-id="5ef95-235">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span><span class="sxs-lookup"><span data-stu-id="5ef95-235">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span></span>
    
- <span data-ttu-id="5ef95-236">document-uri = ubicación URI de documento para abrir</span><span class="sxs-lookup"><span data-stu-id="5ef95-236">document-uri = URI location of document to open</span></span>
    
- <span data-ttu-id="5ef95-237">template-uri = ubicación URI de archivo de plantilla que se usará para el nuevo archivo</span><span class="sxs-lookup"><span data-stu-id="5ef95-237">template-uri = URI location of template file upon which new file will be based</span></span>
    
- <span data-ttu-id="5ef95-238">save-location\* = ubicación URI de carpeta en la que se creará el nuevo documento</span><span class="sxs-lookup"><span data-stu-id="5ef95-238">save-location\* = URI location of folder in which new document should be created</span></span>
    
- <span data-ttu-id="5ef95-239">\*save-location es un parámetro opcional</span><span class="sxs-lookup"><span data-stu-id="5ef95-239">\*save-location is an optional parameter</span></span>
    
### <a name="b-4-uri-scheme-semantics"></a><span data-ttu-id="5ef95-p127">B-4. Semántica del esquema URI</span><span class="sxs-lookup"><span data-stu-id="5ef95-p127">B-4. URI Scheme Semantics</span></span>

<span data-ttu-id="5ef95-p128">El esquema ms-powerpoint define una sintaxis URI para abrir o crear un documento de presentación. El esquema define tres comandos que sirven como instrucciones sobre qué se debe hacer con el documento de referencia. Los comandos son 1) open-for-edit-cmd (ofe), que indica a una aplicación de presentación que abra el documento en el URI especificado para la edición; 2) open-for-view-cmd (ofv), que indica a una aplicación de presentación que abra el documento en el URI especificado en modo de solo lectura; y 3) new-from-template-cmd (nft), que indica a una aplicación de presentación que cree un nuevo documento según la plantilla de documento ubicada en el URI template-uri especificado y guarde el nuevo documento en la ubicación especificada en el URI save-location opcional o, si falta el URI opcional, en la ubicación de la biblioteca de documentos predeterminada.</span><span class="sxs-lookup"><span data-stu-id="5ef95-p128">The ms-powerpoint scheme defines a URI syntax for opening or creating a presentation document. The scheme defines three commands that serve as instructions regarding what should be done with the referenced document. The commands are 1) open-for-edit-cmd (ofe), which instructs a presentation application to open the document at the specified URI for editing; 2) open-for-view-cmd (ofv), which instructs a presentation application to open the document at the specified URI in a read-only mode; and 3) new-from-template-cmd (nft), which instructs a presentation application to create a new document based on the document template located at the specified template-uri URI and save the new document either in the location specified in the optional save-location URI or, in the absence of that optional URI, in the default document library location.</span></span>
  
### <a name="b-5-applicationsprotocols-that-use-the-ms-powerpoint-uri-scheme"></a><span data-ttu-id="5ef95-p129">B-5. Aplicaciones/protocolos que usan el esquema URI ms-powerpoint</span><span class="sxs-lookup"><span data-stu-id="5ef95-p129">B-5. Applications/Protocols that use the ms-powerpoint URI Scheme</span></span>

<span data-ttu-id="5ef95-p130">Microsoft Office 2013 usa el esquema URI ms-powerpoint para invocar Microsoft PowerPoint 2013 o Microsoft PowerPoint 2010 con Service Pack 2. Microsoft SharePoint 2013 usa URI ms-powerpoint como vínculos a documentos de presentación almacenados en bibliotecas de documentos de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="5ef95-p130">The ms-powerpoint URI Scheme is used by Microsoft Office 2013 to invoke Microsoft PowerPoint 2013 or Microsoft PowerPoint 2010 with Service Pack 2. Microsoft SharePoint 2013 uses ms-powerpoint URIs as links to presentation documents stored in SharePoint document libraries.</span></span>
  
### <a name="b-6-interoperability-considerations"></a><span data-ttu-id="5ef95-p131">B-6. Consideraciones de interoperabilidad</span><span class="sxs-lookup"><span data-stu-id="5ef95-p131">B-6. Interoperability Considerations</span></span>

<span data-ttu-id="5ef95-p132">Tenga en cuenta que la barra vertical que se usa como delimitador de esta especificación no se encuentra entre los caracteres identificados en la sección 2.2 de RFC 3986 porque está reservado para uso potencial como delimitadores. Esto se hace intencionalmente para maximizar el conjunto de caracteres que el argumento de comando URI puede admitir sin necesidad de codificar los caracteres con porcentaje.</span><span class="sxs-lookup"><span data-stu-id="5ef95-p132">Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters. This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters.</span></span>
  
<span data-ttu-id="5ef95-253">Dentro de los segmentos < *argumento-comando*  > los caracteres reservados RFC 3986 ":" y "/" forman parte de los datos del argumento, no los delimitadores y por lo tanto, se incluyen sin secuencias de escape.</span><span class="sxs-lookup"><span data-stu-id="5ef95-253">Within < *command-argument*  > segments the RFC 3986 reserved characters ":" and "/" are part of the argument data, not delimiters, and are therefore included unescaped.</span></span> 
  
### <a name="b-7-security-considerations"></a><span data-ttu-id="5ef95-p133">B-7. Consideraciones de seguridad</span><span class="sxs-lookup"><span data-stu-id="5ef95-p133">B-7. Security Considerations</span></span>

<span data-ttu-id="5ef95-p134">En sistemas que tienen controladores registrados para reconocer y actuar en URI ms-powerpoint, al hacer clic en un vínculo a un URI ms-powerpoint, la aplicación de presentación registrada se iniciará, con instrucciones de que la aplicación intente abrir un documento en el URI especificado. Las aplicaciones que se registran para procesar URI ms-powerpoint deben implementar protecciones para protegerse contra la apertura de documentos desde sistemas remotos que no son de confianza y que pueden incluir código malintencionado.</span><span class="sxs-lookup"><span data-stu-id="5ef95-p134">On systems that have registered handlers to recognize and act on ms-powerpoint URIs, clicking on a link to an ms-powerpoint URI will cause the registered presentation application to be launched, with instructions to the application to attempt to open a document at the specified URI. Applications registering to process ms-powerpoint URIs should implement protections to guard against opening documents from untrusted remote systems that may include malicious code.</span></span>
  
### <a name="b-8-references"></a><span data-ttu-id="5ef95-p135">B-8. Referencias</span><span class="sxs-lookup"><span data-stu-id="5ef95-p135">B-8. References</span></span>

<span data-ttu-id="5ef95-260">RFC 3987: Identificadores de recursos internacionales (IRI)</span><span class="sxs-lookup"><span data-stu-id="5ef95-260">RFC 3987 - International Resource Identifiers (IRIs)</span></span>  
  
## <a name="appendix-c---uri-scheme-registration-template-for-ms-excel-scheme"></a><span data-ttu-id="5ef95-261">APÉNDICE C: PLANTILLA DE REGISTRO DE ESQUEMA URI PARA ESQUEMA MS-EXCEL</span><span class="sxs-lookup"><span data-stu-id="5ef95-261">APPENDIX C - URI SCHEME REGISTRATION TEMPLATE FOR MS-EXCEL SCHEME</span></span>
<span data-ttu-id="5ef95-262"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="5ef95-262"></span></span>

### <a name="c-3-uri-scheme-syntax"></a><span data-ttu-id="5ef95-p136">C-3. Sintaxis de esquema URI</span><span class="sxs-lookup"><span data-stu-id="5ef95-p136">C-3. URI Scheme Syntax</span></span>

> <span data-ttu-id="5ef95-265">Esquema de Excel = "ms-excel:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span><span class="sxs-lookup"><span data-stu-id="5ef95-265">Excel Scheme = "ms-excel:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span></span>
    
> <span data-ttu-id="5ef95-266">open-for-edit-cmd = "ofe|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="5ef95-266">open-for-edit-cmd = "ofe|u|" document-uri</span></span>
    
> <span data-ttu-id="5ef95-267">open-for-view-cmd = "ofv|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="5ef95-267">open-for-view-cmd = "ofv|u|" document-uri</span></span>
    
> <span data-ttu-id="5ef95-268">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span><span class="sxs-lookup"><span data-stu-id="5ef95-268">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span></span>
    
> <span data-ttu-id="5ef95-269">document-uri = ubicación URI de documento para abrir</span><span class="sxs-lookup"><span data-stu-id="5ef95-269">document-uri = URI location of document to open</span></span>
    
> <span data-ttu-id="5ef95-270">template-uri = ubicación URI de archivo de plantilla que se usará para el nuevo archivo</span><span class="sxs-lookup"><span data-stu-id="5ef95-270">template-uri = URI location of template file upon which new file will be based</span></span>
    
> <span data-ttu-id="5ef95-271">save-location\* = ubicación URI de carpeta en la que se creará el nuevo documento</span><span class="sxs-lookup"><span data-stu-id="5ef95-271">save-location\* = URI location of folder in which new document should be created</span></span>
    
> <span data-ttu-id="5ef95-272">\*save-location es un parámetro opcional</span><span class="sxs-lookup"><span data-stu-id="5ef95-272">\*save-location is an optional parameter</span></span>
    
### <a name="c-4-uri-scheme-semantics"></a><span data-ttu-id="5ef95-p137">C-4. Semántica del esquema URI</span><span class="sxs-lookup"><span data-stu-id="5ef95-p137">C-4. URI Scheme Semantics</span></span>

<span data-ttu-id="5ef95-p138">El esquema ms-excel define una sintaxis URI para abrir o crear un documento de hoja de cálculo. El esquema define tres comandos que sirven como instrucciones sobre qué se debe hacer con el documento de referencia. Los comandos son 1) open-for-edit-cmd (ofe), que indica a una aplicación de hoja de cálculo que abra el documento en el URI especificado para la edición; 2) open-for-view-cmd (ofv), que indica a una aplicación de hoja de cálculo que abra el documento en el URI especificado en modo de solo lectura; y 3) new-from-template-cmd (nft), que indica a una aplicación de hoja de cálculo que cree un nuevo documento según la plantilla de documento ubicada en el URI template-uri especificado y guarde el nuevo documento en la ubicación especificada en el URI save-location opcional o, si falta el URI opcional, en la ubicación de la biblioteca de documentos predeterminada.</span><span class="sxs-lookup"><span data-stu-id="5ef95-p138">The ms-excel scheme defines a URI syntax for opening or creating a spreadsheet document. The scheme defines three commands that serve as instructions regarding what should be done with the referenced document. The commands are 1) open-for-edit-cmd (ofe), which instructs a spreadsheet application to open the document at the specified URI for editing; 2) open-for-view-cmd (ofv), which instructs a spreadsheet application to open the document at the specified URI in a read-only mode; and 3) new-from-template-cmd (nft), which instructs a spreadsheet application to create a new document based on the document template located at the specified template-uri URI and save the new document either in the location specified in the optional save-location URI or, in the absence of that optional URI, in the default document library location.</span></span>
  
### <a name="c-5-applicationsprotocols-that-use-the-ms-excel-uri-scheme"></a><span data-ttu-id="5ef95-p139">C-5. Aplicaciones/protocolos que usan el esquema URI ms-excel</span><span class="sxs-lookup"><span data-stu-id="5ef95-p139">C-5. Applications/Protocols that use the ms-excel URI Scheme</span></span>

<span data-ttu-id="5ef95-p140">Microsoft Office 2013 usa el esquema URI ms-excel para invocar Microsoft Excel 2013 o Microsoft Excel 2010 con Service Pack 2. Microsoft SharePoint 2013 usa URI ms-excel como vínculos a documentos de hoja de cálculo almacenados en bibliotecas de documentos de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="5ef95-p140">The ms-excel URI Scheme is used by Microsoft Office 2013 to invoke Microsoft Excel 2013 or Microsoft Excel 2010 with Service Pack 2. Microsoft SharePoint 2013 uses ms-excel URIs as links to spreadsheet documents stored in SharePoint document libraries.</span></span>
  
### <a name="c-6-interoperability-considerations"></a><span data-ttu-id="5ef95-p141">C-6. Consideraciones de interoperabilidad</span><span class="sxs-lookup"><span data-stu-id="5ef95-p141">C-6. Interoperability Considerations</span></span>

<span data-ttu-id="5ef95-p142">Tenga en cuenta que la barra vertical que se usa como delimitador de esta especificación no se encuentra entre los caracteres identificados en la sección 2.2 de RFC 3986 porque está reservado para uso potencial como delimitadores. Esto se hace intencionalmente para maximizar el conjunto de caracteres que el argumento de comando URI puede admitir sin necesidad de codificar los caracteres con porcentaje.</span><span class="sxs-lookup"><span data-stu-id="5ef95-p142">Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters. This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters.</span></span>
  
<span data-ttu-id="5ef95-286">Dentro de los segmentos < *argumento-comando*  > los caracteres reservados RFC 3986 ":" y "/" forman parte de los datos del argumento, no los delimitadores y por lo tanto, se incluyen sin secuencias de escape.</span><span class="sxs-lookup"><span data-stu-id="5ef95-286">Within < *command-argument*  > segments the RFC 3986 reserved characters ":" and "/" are part of the argument data, not delimiters, and are therefore included unescaped.</span></span> 
  
### <a name="c-7-security-considerations"></a><span data-ttu-id="5ef95-p143">C-7. Consideraciones de seguridad</span><span class="sxs-lookup"><span data-stu-id="5ef95-p143">C-7. Security Considerations</span></span>

<span data-ttu-id="5ef95-p144">En sistemas que tienen controladores registrados para reconocer y actuar en URI ms-excel, al hacer clic en un vínculo a un URI ms-excel, la aplicación de hoja de cálculo registrada se iniciará, con instrucciones de que la aplicación intente abrir un documento en el URI especificado. Las aplicaciones que se registran para procesar URI ms-excel deben implementar protecciones para protegerse contra la apertura de documentos desde sistemas remotos que no son de confianza y que pueden incluir código malintencionado.</span><span class="sxs-lookup"><span data-stu-id="5ef95-p144">On systems that have registered handlers to recognize and act on ms-excel URIs, clicking on a link to an ms-excel URI will cause the registered spreadsheet application to be launched, with instructions to the application to attempt to open a document at the specified URI. Applications registering to process ms-excel URIs should implement protections to guard against opening documents from untrusted remote systems that may include malicious code.</span></span>
  
### <a name="c-8-references"></a><span data-ttu-id="5ef95-p145">C-8. Referencias</span><span class="sxs-lookup"><span data-stu-id="5ef95-p145">C-8. References</span></span>

<span data-ttu-id="5ef95-293">RFC 3987: Identificadores de recursos internacionales (IRI)</span><span class="sxs-lookup"><span data-stu-id="5ef95-293">RFC 3987 - International Resource Identifiers (IRIs)</span></span>  
  
## <a name="appendix-d---uri-scheme-registration-template-for-ms-visio-scheme"></a><span data-ttu-id="5ef95-294">APÉNDICE D: PLANTILLA DE REGISTRO DE ESQUEMA URI PARA ESQUEMA MS-VISIO</span><span class="sxs-lookup"><span data-stu-id="5ef95-294">APPENDIX D - URI SCHEME REGISTRATION TEMPLATE FOR MS-VISIO SCHEME</span></span>
<span data-ttu-id="5ef95-295"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="5ef95-295"></span></span>

### <a name="d-3-uri-scheme-syntax"></a><span data-ttu-id="5ef95-p146">D-3. Sintaxis de esquema URI</span><span class="sxs-lookup"><span data-stu-id="5ef95-p146">D-3. URI Scheme Syntax</span></span>

> <span data-ttu-id="5ef95-298">Esquema de Visio = "ms-visio:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span><span class="sxs-lookup"><span data-stu-id="5ef95-298">Visio Scheme = "ms-visio:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span></span>
    
> <span data-ttu-id="5ef95-299">open-for-edit-cmd = "ofe|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="5ef95-299">open-for-edit-cmd = "ofe|u|" document-uri</span></span>
    
> <span data-ttu-id="5ef95-300">open-for-view-cmd = "ofv|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="5ef95-300">open-for-view-cmd = "ofv|u|" document-uri</span></span>
    
> <span data-ttu-id="5ef95-301">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span><span class="sxs-lookup"><span data-stu-id="5ef95-301">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span></span>
    
> <span data-ttu-id="5ef95-302">document-uri = ubicación URI de documento para abrir</span><span class="sxs-lookup"><span data-stu-id="5ef95-302">document-uri = URI location of document to open</span></span>
    
> <span data-ttu-id="5ef95-303">template-uri = ubicación URI de archivo de plantilla que se usará para el nuevo archivo</span><span class="sxs-lookup"><span data-stu-id="5ef95-303">template-uri = URI location of template file upon which new file will be based</span></span>
    
> <span data-ttu-id="5ef95-304">save-location\* = ubicación URI de carpeta en la que se creará el nuevo documento</span><span class="sxs-lookup"><span data-stu-id="5ef95-304">save-location\* = URI location of folder in which new document should be created</span></span>
    
> <span data-ttu-id="5ef95-305">\*save-location es un parámetro opcional</span><span class="sxs-lookup"><span data-stu-id="5ef95-305">\*save-location is an optional parameter</span></span>
    
### <a name="d-4-uri-scheme-semantics"></a><span data-ttu-id="5ef95-p147">D-4. Semántica de esquema URI</span><span class="sxs-lookup"><span data-stu-id="5ef95-p147">D-4. URI Scheme Semantics</span></span>

<span data-ttu-id="5ef95-p148">El esquema ms-visio define una sintaxis URI para abrir o crear un documento de Microsoft Visio. El esquema define tres comandos que sirven como instrucciones sobre qué se debe hacer con el documento de referencia. Los comandos son 1) open-for-edit-cmd (ofe), que indica a Visio que abra el documento en el URI especificado para la edición; 2) open-for-view-cmd (ofv), que indica a Visio que abra el documento en el URI especificado en modo de solo lectura; y 3) new-from-template-cmd (nft), que indica a Visio que cree un nuevo documento según la plantilla de documento ubicada en el URI template-uri especificado y guarde el nuevo documento en la ubicación especificada en el URI save-location opcional o, si falta el URI opcional, en la ubicación de la biblioteca de documentos predeterminada.</span><span class="sxs-lookup"><span data-stu-id="5ef95-p148">The ms-visio scheme defines a URI syntax for opening or creating a Microsoft Visio document. The scheme defines three commands that serve as instructions regarding what should be done with the referenced document. The commands are 1) open-for-edit-cmd (ofe), which instructs Visio to open the document at the specified URI for editing; 2) open-for-view-cmd (ofv), which instructs Visio to open the document at the specified URI in a read-only mode; and 3) new-from-template-cmd (nft), which instructs Visio to create a new document based on the document template located at the specified template-uri URI and save the new document either in the location specified in the optional save-location URI or, in the absence of that optional URI, in the default document library location.</span></span>
  
### <a name="d-5-applicationsprotocols-that-use-the-ms-visio-uri-scheme"></a><span data-ttu-id="5ef95-p149">D-5. Aplicaciones/protocolos que usan el esquema URI ms-visio</span><span class="sxs-lookup"><span data-stu-id="5ef95-p149">D-5. Applications/Protocols that use the ms-visio URI Scheme</span></span>

<span data-ttu-id="5ef95-p150">Microsoft Office 2013 usa el esquema URI ms-visio para invocar Microsoft Visio 2013 o Microsoft Visio 2010 con Service Pack 2. Microsoft SharePoint 2013 usa URI ms-visio como vínculos a documentos de Visio almacenados en bibliotecas de documentos de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="5ef95-p150">The ms-visio URI Scheme is used by Microsoft Office 2013 to invoke Microsoft Visio 2013 or Microsoft Visio 2010 with Service Pack 2. Microsoft SharePoint 2013 uses ms-visio URIs as links to Visio documents stored in SharePoint document libraries.</span></span>
  
### <a name="d-6-interoperability-considerations"></a><span data-ttu-id="5ef95-p151">D-6. Consideraciones de interoperabilidad</span><span class="sxs-lookup"><span data-stu-id="5ef95-p151">D-6. Interoperability Considerations</span></span>

<span data-ttu-id="5ef95-p152">Tenga en cuenta que la barra vertical que se usa como delimitador de esta especificación no se encuentra entre los caracteres identificados en la sección 2.2 de RFC 3986 porque está reservado para uso potencial como delimitadores. Esto se hace intencionalmente para maximizar el conjunto de caracteres que el argumento de comando URI puede admitir sin necesidad de codificar los caracteres con porcentaje.</span><span class="sxs-lookup"><span data-stu-id="5ef95-p152">Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters. This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters.</span></span>
  
<span data-ttu-id="5ef95-319">Dentro de los segmentos < *argumento-comando*  > los caracteres reservados RFC 3986 ":" y "/" forman parte de los datos del argumento, no los delimitadores y por lo tanto, se incluyen sin secuencias de escape.</span><span class="sxs-lookup"><span data-stu-id="5ef95-319">Within < *command-argument*  > segments the RFC 3986 reserved characters ":" and "/" are part of the argument data, not delimiters, and are therefore included unescaped.</span></span> 
  
### <a name="d-7-security-considerations"></a><span data-ttu-id="5ef95-p153">D-7. Consideraciones de seguridad</span><span class="sxs-lookup"><span data-stu-id="5ef95-p153">D-7. Security Considerations</span></span>

<span data-ttu-id="5ef95-p154">En sistemas que tienen controladores registrados para reconocer y actuar en URI ms-visio, al hacer clic en un vínculo a un URI ms-visio, la aplicación registrada se iniciará, con instrucciones de que la aplicación intente abrir un documento en el URI especificado. Las aplicaciones que se registran para procesar URI ms-visio deben implementar protecciones para protegerse contra la apertura de documentos desde sistemas remotos que no son de confianza y que pueden incluir código malintencionado.</span><span class="sxs-lookup"><span data-stu-id="5ef95-p154">On systems that have registered handlers to recognize and act on ms-visio URIs, clicking on a link to an ms-visio URI will cause the registered application to be launched, with instructions to the application to attempt to open a document at the specified URI. Applications registering to process ms-visio URIs should implement protections to guard against opening documents from untrusted remote systems that may include malicious code.</span></span>
  
### <a name="d-8-references"></a><span data-ttu-id="5ef95-p155">D-8. Referencias</span><span class="sxs-lookup"><span data-stu-id="5ef95-p155">D-8. References</span></span>

<span data-ttu-id="5ef95-326">RFC 3987: Identificadores de recursos internacionales (IRI)</span><span class="sxs-lookup"><span data-stu-id="5ef95-326">RFC 3987 - International Resource Identifiers (IRIs)</span></span>
  
## <a name="appendix-e---uri-scheme-registration-template-for-ms-access-scheme"></a><span data-ttu-id="5ef95-327">APÉNDICE E: PLANTILLA DE REGISTRO DE ESQUEMA URI PARA ESQUEMA MS-ACCESS</span><span class="sxs-lookup"><span data-stu-id="5ef95-327">APPENDIX E - URI SCHEME REGISTRATION TEMPLATE FOR MS-ACCESS SCHEME</span></span>
<span data-ttu-id="5ef95-328"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="5ef95-328"></span></span>

### <a name="e-3-uri-scheme-syntax"></a><span data-ttu-id="5ef95-p156">E-3. Sintaxis de esquema URI</span><span class="sxs-lookup"><span data-stu-id="5ef95-p156">E-3. URI Scheme Syntax</span></span>

> <span data-ttu-id="5ef95-331">Esquema de Access = "ms-access:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span><span class="sxs-lookup"><span data-stu-id="5ef95-331">Access Scheme = "ms-access:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span></span>
    
> <span data-ttu-id="5ef95-332">open-for-edit-cmd = "ofe|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="5ef95-332">open-for-edit-cmd = "ofe|u|" document-uri</span></span>
    
> <span data-ttu-id="5ef95-333">open-for-view-cmd = "ofv|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="5ef95-333">open-for-view-cmd = "ofv|u|" document-uri</span></span>
    
> <span data-ttu-id="5ef95-334">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span><span class="sxs-lookup"><span data-stu-id="5ef95-334">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span></span>
    
> <span data-ttu-id="5ef95-335">document-uri = ubicación URI de documento para abrir</span><span class="sxs-lookup"><span data-stu-id="5ef95-335">document-uri = URI location of document to open</span></span>
    
> <span data-ttu-id="5ef95-336">template-uri = ubicación URI de archivo de plantilla que se usará para el nuevo archivo</span><span class="sxs-lookup"><span data-stu-id="5ef95-336">template-uri = URI location of template file upon which new file will be based</span></span>
    
> <span data-ttu-id="5ef95-337">save-location\* = ubicación URI de carpeta en la que se creará el nuevo documento</span><span class="sxs-lookup"><span data-stu-id="5ef95-337">save-location\* = URI location of folder in which new document should be created</span></span>
    
> <span data-ttu-id="5ef95-338">\*save-location es un parámetro opcional</span><span class="sxs-lookup"><span data-stu-id="5ef95-338">\*save-location is an optional parameter</span></span>
    
### <a name="e-4-uri-scheme-semantics"></a><span data-ttu-id="5ef95-p157">E-4. Semántica de esquema URI</span><span class="sxs-lookup"><span data-stu-id="5ef95-p157">E-4. URI Scheme Semantics</span></span>

<span data-ttu-id="5ef95-p158">El esquema ms-access define una sintaxis URI para abrir o crear una base de datos. El esquema define tres comandos que sirven como instrucciones sobre qué se debe hacer con el archivo de base de datos de referencia. Los comandos son 1) open-for-edit-cmd (ofe), que indica a una aplicación de base de datos que abra la base de datos en el URI especificado para la edición; 2) open-for-view-cmd (ofv), que indica a una aplicación de base de datos que abra la base de datos en el URI especificado en modo de solo lectura; y 3) new-from-template-cmd (nft), que indica a la aplicación de base de datos que cree una nueva base de datos según la plantilla ubicada en el URI template-uri especificado y guarde la nueva base de datos en la ubicación especificada en el URI save-location opcional o, si falta el URI opcional, en la ubicación de la biblioteca de documentos predeterminada.</span><span class="sxs-lookup"><span data-stu-id="5ef95-p158">The ms-access scheme defines a URI syntax for opening or creating a database. The scheme defines three commands that serve as instructions regarding what should be done with the referenced database file. The commands are 1) open-for-edit-cmd (ofe), which instructs the database application to open the database at the specified URI for editing; 2) open-for-view-cmd (ofv), which instructs the database application to open the database at the specified URI in a read-only mode; and 3) new-from-template-cmd (nft), which instructs the database application to create a new database based on the template located at the specified template-uri URI and save the new database either in the location specified in the optional save-location URI or, in the absence of that optional URI, in the default document library location.</span></span>
  
### <a name="e-5-applicationsprotocols-that-use-the-ms-access-uri-scheme"></a><span data-ttu-id="5ef95-p159">E-5. Aplicaciones/protocolos que usan el esquema URI ms-access</span><span class="sxs-lookup"><span data-stu-id="5ef95-p159">E-5. Applications/Protocols that use the ms-access URI Scheme</span></span>

<span data-ttu-id="5ef95-p160">Microsoft Office 2013 usa el esquema URI ms-access para invocar Microsoft Access 2013 o Microsoft Access 2010 con Service Pack 2 desde páginas web. Microsoft SharePoint 2013 usa URI ms-access como vínculos a bases de datos de Access almacenadas en bibliotecas de documentos de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="5ef95-p160">The ms-access URI Scheme is used by Microsoft Office 2013 to invoke Microsoft Access 2013 or Microsoft Access 2010 with Service Pack 2 from web pages. Microsoft SharePoint 2013 uses ms-access URIs as links to Access databases stored in SharePoint document libraries.</span></span>
  
### <a name="e-6-interoperability-considerations"></a><span data-ttu-id="5ef95-p161">E-6. Consideraciones de interoperabilidad</span><span class="sxs-lookup"><span data-stu-id="5ef95-p161">E-6. Interoperability Considerations</span></span>

<span data-ttu-id="5ef95-p162">Tenga en cuenta que la barra vertical que se usa como delimitador de esta especificación no se encuentra entre los caracteres identificados en la sección 2.2 de RFC 3986 porque está reservado para uso potencial como delimitadores. Esto se hace intencionalmente para maximizar el conjunto de caracteres que el argumento de comando URI puede admitir sin necesidad de codificar los caracteres con porcentaje. Dentro de los segmentos \<argumento-comando\> los caracteres reservados RFC 3986 ":" y "/" forman parte de los datos del argumento, no los delimitadores y por lo tanto, se incluyen sin secuencias de escape.</span><span class="sxs-lookup"><span data-stu-id="5ef95-p162">Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters. This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters. Within \<command-argument\> segments the RFC 3986 reserved characters ":" and "/" are part of the argument data, not delimiters, and are therefore included unescaped.</span></span>
  
### <a name="e-7-security-considerations"></a><span data-ttu-id="5ef95-p163">E-7. Consideraciones de seguridad</span><span class="sxs-lookup"><span data-stu-id="5ef95-p163">E-7. Security Considerations</span></span>

<span data-ttu-id="5ef95-p164">En sistemas que tienen controladores registrados para reconocer y actuar en URI ms-access, al hacer clic en un vínculo a un URI ms-access, la aplicación registrada se iniciará, con instrucciones de que la aplicación intente abrir una base de datos en el URI especificado. Las aplicaciones que se registran para procesar URI ms-access deben implementar protecciones para protegerse contra la apertura de bases de datos desde sistemas remotos que no son de confianza y que pueden incluir código malintencionado.</span><span class="sxs-lookup"><span data-stu-id="5ef95-p164">On systems that have registered handlers to recognize and act on ms-access URIs, clicking on a link to an ms-access URI will cause the registered application to be launched, with instructions to the application to attempt to open a database at the specified URI. Applications registering to process ms-access URIs should implement protections to guard against opening databases from untrusted remote systems that may include malicious code.</span></span>
  
### <a name="e-8-references"></a><span data-ttu-id="5ef95-p165">E-8. Referencias</span><span class="sxs-lookup"><span data-stu-id="5ef95-p165">E-8. References</span></span>

<span data-ttu-id="5ef95-359">RFC 3987: Identificadores de recursos internacionales (IRI)</span><span class="sxs-lookup"><span data-stu-id="5ef95-359">RFC 3987 - International Resource Identifiers (IRIs)</span></span>  
  
## <a name="appendix-f---uri-scheme-registration-template-for-ms-project-scheme"></a><span data-ttu-id="5ef95-360">APÉNDICE F: PLANTILLA DE REGISTRO DE ESQUEMA URI PARA ESQUEMA MS-PROJECT</span><span class="sxs-lookup"><span data-stu-id="5ef95-360">APPENDIX F - URI SCHEME REGISTRATION TEMPLATE FOR MS-PROJECT SCHEME</span></span>
<span data-ttu-id="5ef95-361"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="5ef95-361"></span></span>

### <a name="f-3-uri-scheme-syntax"></a><span data-ttu-id="5ef95-p166">F-3. Sintaxis de esquema URI</span><span class="sxs-lookup"><span data-stu-id="5ef95-p166">F-3. URI Scheme Syntax</span></span>

> <span data-ttu-id="5ef95-364">Esquema de Project = "ms-project:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span><span class="sxs-lookup"><span data-stu-id="5ef95-364">Project Scheme = "ms-project:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span></span>
    
> <span data-ttu-id="5ef95-365">open-for-edit-cmd = "ofe|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="5ef95-365">open-for-edit-cmd = "ofe|u|" document-uri</span></span>
    
> <span data-ttu-id="5ef95-366">open-for-view-cmd = "ofv|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="5ef95-366">open-for-view-cmd = "ofv|u|" document-uri</span></span>
    
> <span data-ttu-id="5ef95-367">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span><span class="sxs-lookup"><span data-stu-id="5ef95-367">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span></span>
    
> <span data-ttu-id="5ef95-368">document-uri = ubicación URI de documento para abrir</span><span class="sxs-lookup"><span data-stu-id="5ef95-368">document-uri = URI location of document to open</span></span>
    
> <span data-ttu-id="5ef95-369">template-uri = ubicación URI de archivo de plantilla que se usará para el nuevo archivo</span><span class="sxs-lookup"><span data-stu-id="5ef95-369">template-uri = URI location of template file upon which new file will be based</span></span>
    
> <span data-ttu-id="5ef95-370">save-location\* = ubicación URI de carpeta en la que se creará el nuevo documento</span><span class="sxs-lookup"><span data-stu-id="5ef95-370">save-location\* = URI location of folder in which new document should be created</span></span>
    
> <span data-ttu-id="5ef95-371">\*save-location es un parámetro opcional</span><span class="sxs-lookup"><span data-stu-id="5ef95-371">\*save-location is an optional parameter</span></span>
    
### <a name="f-4-uri-scheme-semantics"></a><span data-ttu-id="5ef95-p167">F-4. Semántica del esquema URI</span><span class="sxs-lookup"><span data-stu-id="5ef95-p167">F-4. URI Scheme Semantics</span></span>

<span data-ttu-id="5ef95-p168">El esquema ms-project define una sintaxis URI para abrir o crear un documento de Microsoft Project. El esquema define tres comandos que sirven como instrucciones sobre qué se debe hacer con el documento de referencia. Los comandos son 1) open-for-edit-cmd (ofe), que indica a Project que abra el documento en el URI especificado para la edición; 2) open-for-view-cmd (ofv), que indica a Project que abra el documento en el URI especificado en modo de solo lectura; y 3) new-from-template-cmd (nft), que indica a Project que cree un nuevo documento según la plantilla de documento ubicada en el URI template-uri especificado y guarde el nuevo documento en la ubicación especificada en el URI save-location opcional o, si falta el URI opcional, en la ubicación de la biblioteca de documentos predeterminada.</span><span class="sxs-lookup"><span data-stu-id="5ef95-p168">The ms-project scheme defines a URI syntax for opening or creating a Microsoft Project document. The scheme defines three commands that serve as instructions regarding what should be done with the referenced document. The commands are 1) open-for-edit-cmd (ofe), which instructs Project to open the document at the specified URI for editing; 2) open-for-view-cmd (ofv), which instructs Project to open the document at the specified URI in a read-only mode; and 3) new-from-template-cmd (nft), which instructs Project to create a new document based on the document template located at the specified template-uri URI and save the new document either in the location specified in the optional save-location URI or, in the absence of that optional URI, in the default document library location.</span></span>
  
### <a name="f-5-applicationsprotocols-that-use-the-ms-project-uri-scheme"></a><span data-ttu-id="5ef95-p169">F-5. Aplicaciones/protocolos que usan el esquema URI ms-project</span><span class="sxs-lookup"><span data-stu-id="5ef95-p169">F-5. Applications/Protocols that use the ms-project URI Scheme</span></span>

<span data-ttu-id="5ef95-p170">Microsoft Office 2013 usa el esquema URI ms-project para invocar Microsoft Project 2013 desde páginas web. Microsoft SharePoint 2013 usa URI ms-project como vínculos a documentos de Project almacenados en bibliotecas de documentos de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="5ef95-p170">The ms-project URI Scheme is used by Microsoft Office 2013 to invoke Microsoft Project 2013 from web pages. Microsoft SharePoint 2013 uses ms-project URIs as links to Project documents stored in SharePoint document libraries.</span></span>
  
### <a name="f-6-interoperability-considerations"></a><span data-ttu-id="5ef95-p171">F-6. Consideraciones de interoperabilidad</span><span class="sxs-lookup"><span data-stu-id="5ef95-p171">F-6. Interoperability Considerations</span></span>

<span data-ttu-id="5ef95-p172">Tenga en cuenta que la barra vertical que se usa como delimitador de esta especificación no se encuentra entre los caracteres identificados en la sección 2.2 de RFC 3986 porque está reservado para uso potencial como delimitadores. Esto se hace intencionalmente para maximizar el conjunto de caracteres que el argumento de comando URI puede admitir sin necesidad de codificar los caracteres con porcentaje.</span><span class="sxs-lookup"><span data-stu-id="5ef95-p172">Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters. This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters.</span></span>
  
<span data-ttu-id="5ef95-385">Dentro de los segmentos < *argumento-comando*  > los caracteres reservados RFC 3986 ":" y "/" forman parte de los datos del argumento, no los delimitadores y por lo tanto, se incluyen sin secuencias de escape.</span><span class="sxs-lookup"><span data-stu-id="5ef95-385">Within < *command-argument*  > segments the RFC 3986 reserved characters ":" and "/" are part of the argument data, not delimiters, and are therefore included unescaped.</span></span> 
  
### <a name="f-7-security-considerations"></a><span data-ttu-id="5ef95-p173">F-7. Consideraciones de seguridad</span><span class="sxs-lookup"><span data-stu-id="5ef95-p173">F-7. Security Considerations</span></span>

<span data-ttu-id="5ef95-p174">En sistemas que tienen controladores registrados para reconocer y actuar en URI ms-project, al hacer clic en un vínculo a un URI ms-project, la aplicación registrada se iniciará, con instrucciones de que la aplicación intente abrir un documento en el URI especificado. Las aplicaciones que se registran para procesar URI ms-project deben implementar protecciones para protegerse contra la apertura de documentos desde sistemas remotos que no son de confianza y que pueden incluir código malintencionado.</span><span class="sxs-lookup"><span data-stu-id="5ef95-p174">On systems that have registered handlers to recognize and act on ms-project URIs, clicking on a link to an ms-project URI will cause the registered application to be launched, with instructions to the application to attempt to open a document at the specified URI. Applications registering to process ms-project URIs should implement protections to guard against opening documents from untrusted remote systems that may include malicious code.</span></span>
  
### <a name="f-8-references"></a><span data-ttu-id="5ef95-p175">F-8. Referencias</span><span class="sxs-lookup"><span data-stu-id="5ef95-p175">F-8. References</span></span>

<span data-ttu-id="5ef95-392">RFC 3987: Identificadores de recursos internacionales (IRI)</span><span class="sxs-lookup"><span data-stu-id="5ef95-392">RFC 3987 - International Resource Identifiers (IRIs)</span></span>  
  
## <a name="appendix-g---uri-scheme-registration-template-for-ms-publisher-scheme"></a><span data-ttu-id="5ef95-393">APÉNDICE G: PLANTILLA DE REGISTRO DE ESQUEMA URI PARA ESQUEMA MS-PUBLISHER</span><span class="sxs-lookup"><span data-stu-id="5ef95-393">APPENDIX G - URI SCHEME REGISTRATION TEMPLATE FOR MS-PUBLISHER SCHEME</span></span>
<span data-ttu-id="5ef95-394"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="5ef95-394"></span></span>

### <a name="g-3-uri-scheme"></a><span data-ttu-id="5ef95-p176">G-3. Esquema URI</span><span class="sxs-lookup"><span data-stu-id="5ef95-p176">G-3. URI Scheme</span></span>

> <span data-ttu-id="5ef95-397">Sintaxis de esquema de Publisher = "ms-publisher:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span><span class="sxs-lookup"><span data-stu-id="5ef95-397">Syntax Publisher Scheme = "ms-publisher:" open-for-edit-cmd | open-for-view-cmd | new-from-template-cmd</span></span>
    
> <span data-ttu-id="5ef95-398">open-for-edit-cmd = "ofe|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="5ef95-398">open-for-edit-cmd = "ofe|u|" document-uri</span></span>
    
> <span data-ttu-id="5ef95-399">open-for-view-cmd = "ofv|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="5ef95-399">open-for-view-cmd = "ofv|u|" document-uri</span></span>
    
> <span data-ttu-id="5ef95-400">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span><span class="sxs-lookup"><span data-stu-id="5ef95-400">new-from-template-cmd = "nft|u|" template-uri ["|s|" save-location]</span></span>
    
> <span data-ttu-id="5ef95-401">document-uri = ubicación URI de documento para abrir</span><span class="sxs-lookup"><span data-stu-id="5ef95-401">document-uri = URI location of document to open</span></span>
    
> <span data-ttu-id="5ef95-402">template-uri = ubicación URI de archivo de plantilla que se usará para el nuevo archivo</span><span class="sxs-lookup"><span data-stu-id="5ef95-402">template-uri = URI location of template file upon which new file will be based</span></span>
    
> <span data-ttu-id="5ef95-403">save-location\* = ubicación URI de carpeta en la que se creará el nuevo documento</span><span class="sxs-lookup"><span data-stu-id="5ef95-403">save-location\* = URI location of folder in which new document should be created</span></span>
    
> <span data-ttu-id="5ef95-404">\*save-location es un parámetro opcional</span><span class="sxs-lookup"><span data-stu-id="5ef95-404">\*save-location is an optional parameter</span></span>
    
### <a name="g-4-uri-scheme-semantics"></a><span data-ttu-id="5ef95-p177">G-4. Semántica del esquema URI</span><span class="sxs-lookup"><span data-stu-id="5ef95-p177">G-4. URI Scheme Semantics</span></span>

<span data-ttu-id="5ef95-p178">El esquema ms-publisher define una sintaxis URI para abrir o crear un documento de Microsoft Publisher. El esquema define tres comandos que sirven como instrucciones sobre qué se debe hacer con el documento de referencia. Los comandos son 1) open-for-edit-cmd (ofe), que indica a Publisher que abra el documento en el URI especificado para la edición; 2) open-for-view-cmd (ofv), que indica a Publisher que abra el documento en el URI especificado en modo de solo lectura; y 3) new-from-template-cmd (nft), que indica a Publisher que cree un nuevo documento según la plantilla de documento ubicada en el URI template-uri especificado y guarde el nuevo documento en la ubicación especificada en el URI save-location opcional o, si falta el URI opcional, en la ubicación de la biblioteca de documentos predeterminada.</span><span class="sxs-lookup"><span data-stu-id="5ef95-p178">The ms-publisher scheme defines a URI syntax for opening or creating a Microsoft Publisher document. The scheme defines three commands that serve as instructions regarding what should be done with the referenced document. The commands are 1) open-for-edit-cmd (ofe), which instructs Publisher to open the document at the specified URI for editing; 2) open-for-view-cmd (ofv), which instructs Publisher to open the document at the specified URI in a read-only mode; and 3) new-from-template-cmd (nft), which instructs Publisher to create a new document based on the document template located at the specified template-uri URI and save the new document either in the location specified in the optional save-location URI or, in the absence of that optional URI, in the default document library location.</span></span>
  
### <a name="g-5-applicationsprotocols-that-use-the-ms-publisher-uri-scheme"></a><span data-ttu-id="5ef95-p179">G-5. Aplicaciones/protocolos que usan el esquema URI ms-publisher</span><span class="sxs-lookup"><span data-stu-id="5ef95-p179">G-5. Applications/Protocols that use the ms-publisher URI Scheme</span></span>

<span data-ttu-id="5ef95-p180">Microsoft Office 2013 usa el esquema URI ms-publisher para invocar Microsoft Publisher 2013 o Microsoft Publisher 2010 con Service Pack 2 desde páginas web. Microsoft SharePoint 2013 usa URI ms-publisher como vínculos a documentos de Publisher almacenados en bibliotecas de documentos de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="5ef95-p180">The ms-publisher URI Scheme is used by Microsoft Office 2013 to invoke Microsoft Publisher 2013 or Microsoft Publisher 2010 with Service Pack 2 from web pages. Microsoft SharePoint 2013 uses ms-publisher URIs as links to Publisher documents stored in SharePoint document libraries.</span></span>
  
### <a name="g-6-interoperability-considerations"></a><span data-ttu-id="5ef95-p181">G-6. Consideraciones de interoperabilidad</span><span class="sxs-lookup"><span data-stu-id="5ef95-p181">G-6. Interoperability Considerations</span></span>

<span data-ttu-id="5ef95-p182">Tenga en cuenta que la barra vertical que se usa como delimitador de esta especificación no se encuentra entre los caracteres identificados en la sección 2.2 de RFC 3986 porque está reservado para uso potencial como delimitadores. Esto se hace intencionalmente para maximizar el conjunto de caracteres que el argumento de comando URI puede admitir sin necesidad de codificar los caracteres con porcentaje. Dentro de los segmentos \<argumento-comando\> los caracteres reservados RFC 3986 ":" y "/" forman parte de los datos del argumento, no los delimitadores y por lo tanto, se incluyen sin secuencias de escape.</span><span class="sxs-lookup"><span data-stu-id="5ef95-p182">Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters. This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters. Within \<command-argument\> segments the RFC 3986 reserved characters ":" and "/" are part of the argument data, not delimiters, and are therefore included unescaped.</span></span>
  
### <a name="g-7-security-considerations"></a><span data-ttu-id="5ef95-p183">G-7. Consideraciones de seguridad</span><span class="sxs-lookup"><span data-stu-id="5ef95-p183">G-7. Security Considerations</span></span>

<span data-ttu-id="5ef95-p184">En sistemas que tienen controladores registrados para reconocer y actuar en URI ms-publisher, al hacer clic en un vínculo a un URI ms-publisher, la aplicación registrada se iniciará, con instrucciones de que la aplicación intente abrir un documento en el URI especificado. Las aplicaciones que se registran para procesar URI ms-publisher deben implementar protecciones para protegerse contra la apertura de documentos desde sistemas remotos que no son de confianza y que pueden incluir código malintencionado.</span><span class="sxs-lookup"><span data-stu-id="5ef95-p184">On systems that have registered handlers to recognize and act on ms-publisher URIs, clicking on a link to an ms-publisher URI will cause the registered application to be launched, with instructions to the application to attempt to open a document at the specified URI. Applications registering to process ms-publisher URIs should implement protections to guard against opening documents from untrusted remote systems that may include malicious code.</span></span>
  
### <a name="g-9-references"></a><span data-ttu-id="5ef95-p185">G-9. Referencias</span><span class="sxs-lookup"><span data-stu-id="5ef95-p185">G-9. References</span></span>

<span data-ttu-id="5ef95-425">RFC 3987: Identificadores de recursos internacionales (IRI)</span><span class="sxs-lookup"><span data-stu-id="5ef95-425">RFC 3987 - International Resource Identifiers (IRIs)</span></span>  
  
## <a name="appendix-h---uri-scheme-registration-template-for-ms-spd-scheme"></a><span data-ttu-id="5ef95-426">APÉNDICE H: PLANTILLA DE REGISTRO DE ESQUEMA URI PARA ESQUEMA MS-SPD</span><span class="sxs-lookup"><span data-stu-id="5ef95-426">APPENDIX H - URI SCHEME REGISTRATION TEMPLATE FOR MS-SPD SCHEME</span></span>
<span data-ttu-id="5ef95-427"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="5ef95-427"></span></span>

### <a name="h-3-uri-scheme-syntax"></a><span data-ttu-id="5ef95-p186">H-3. Sintaxis de esquema URI</span><span class="sxs-lookup"><span data-stu-id="5ef95-p186">H-3. URI Scheme Syntax</span></span>

> <span data-ttu-id="5ef95-430">Esquema de SharePoint Designer = "ms-spd:" open-for-edit-cmd</span><span class="sxs-lookup"><span data-stu-id="5ef95-430">SharePoint Designer Scheme = "ms-spd:" open-for-edit-cmd</span></span>
    
> <span data-ttu-id="5ef95-431">open-for-edit-cmd = "ofe|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="5ef95-431">open-for-edit-cmd = "ofe|u|" document-uri</span></span>
    
> <span data-ttu-id="5ef95-432">document-uri = ubicación URI de documento para abrir</span><span class="sxs-lookup"><span data-stu-id="5ef95-432">document-uri = URI location of document to open</span></span>
    
### <a name="h-4-uri-scheme-semantics"></a><span data-ttu-id="5ef95-p187">H-4. Semántica de esquema URI</span><span class="sxs-lookup"><span data-stu-id="5ef95-p187">H-4. URI Scheme Semantics</span></span>

<span data-ttu-id="5ef95-p188">El esquema ms-spd define una sintaxis URI para abrir un documento de Microsoft SharePoint Designer. El esquema define dos comandos que sirven como instrucciones sobre qué se debe hacer con el documento de referencia. Los comandos son 1) open-for-edit-cmd (ofe), que indica a SharePoint Designer que abra el documento en el URI especificado para la edición; y 2) open-for-view-cmd (ofv), que indica a SharePoint Designer que abra el documento en el URI especificado en modo de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5ef95-p188">The ms-spd scheme defines a URI syntax for opening a Microsoft SharePoint Designer document. The scheme defines two commands that serve as instructions regarding what should be done with the referenced document. The commands are 1) open-for-edit-cmd (ofe), which instructs SharePoint Designer to open the document at the specified URI for editing; and 2) open-for-view-cmd (ofv), which instructs SharePoint Designer to open the document at the specified URI in a read-only mode.</span></span>
  
### <a name="h-5-applicationsprotocols-that-use-the-ms-spd-uri-scheme"></a><span data-ttu-id="5ef95-p189">H-5. Aplicaciones/protocolos que usan el esquema URI ms-spd</span><span class="sxs-lookup"><span data-stu-id="5ef95-p189">H-5. Applications/Protocols that use the ms-spd URI Scheme</span></span>

<span data-ttu-id="5ef95-p190">Microsoft Office 2013 usa el esquema URI ms-spd para invocar Microsoft SharePoint Designer 2013 desde páginas web. Microsoft SharePoint 2013 usa URI ms-spd como vínculos a documentos de SharePoint Designer almacenados en bibliotecas de documentos de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="5ef95-p190">The ms-spd URI Scheme is used by Microsoft Office 2013 to invoke Microsoft SharePoint Designer 2013 from web pages. Microsoft SharePoint 2013 uses ms-spd URIs as links to SharePoint Designer documents stored in SharePoint document libraries.</span></span>
  
### <a name="h-6-interoperability-considerations"></a><span data-ttu-id="5ef95-p191">H-6. Consideraciones de interoperabilidad</span><span class="sxs-lookup"><span data-stu-id="5ef95-p191">H-6. Interoperability Considerations</span></span>

<span data-ttu-id="5ef95-p192">Tenga en cuenta que la barra vertical que se usa como delimitador de esta especificación no se encuentra entre los caracteres identificados en la sección 2.2 de RFC 3986 porque está reservado para uso potencial como delimitadores. Esto se hace intencionalmente para maximizar el conjunto de caracteres que el argumento de comando URI puede admitir sin necesidad de codificar los caracteres con porcentaje.</span><span class="sxs-lookup"><span data-stu-id="5ef95-p192">Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters. This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters.</span></span>
  
<span data-ttu-id="5ef95-446">Dentro de los segmentos < *argumento-comando*  > los caracteres reservados RFC 3986 ":" y "/" forman parte de los datos del argumento, no los delimitadores y por lo tanto, se incluyen sin secuencias de escape.</span><span class="sxs-lookup"><span data-stu-id="5ef95-446">Within < *command-argument*  > segments the RFC 3986 reserved characters ":" and "/" are part of the argument data, not delimiters, and are therefore included unescaped.</span></span> 
  
### <a name="h-7-security-considerations"></a><span data-ttu-id="5ef95-p193">H-7. Consideraciones de seguridad</span><span class="sxs-lookup"><span data-stu-id="5ef95-p193">H-7. Security Considerations</span></span>

<span data-ttu-id="5ef95-p194">En sistemas que tienen controladores registrados para reconocer y actuar en URI ms-spd, al hacer clic en un vínculo a un URI ms-spd, la aplicación registrada se iniciará, con instrucciones de que la aplicación intente abrir un documento en el URI especificado. Las aplicaciones que se registran para procesar URI ms-spd deben implementar protecciones para protegerse contra la apertura de documentos desde sistemas remotos que no son de confianza y que pueden incluir código malintencionado.</span><span class="sxs-lookup"><span data-stu-id="5ef95-p194">On systems that have registered handlers to recognize and act on ms-spd URIs, clicking on a link to an ms-spd URI will cause the registered application to be launched, with instructions to the application to attempt to open a document at the specified URI. Applications registering to process ms-spd URIs should implement protections to guard against opening documents from untrusted remote systems that may include malicious code.</span></span>
  
### <a name="h-8-references"></a><span data-ttu-id="5ef95-p195">H-8. Referencias</span><span class="sxs-lookup"><span data-stu-id="5ef95-p195">H-8. References</span></span>

<span data-ttu-id="5ef95-453">RFC 3987: Identificadores de recursos internacionales (IRI)</span><span class="sxs-lookup"><span data-stu-id="5ef95-453">RFC 3987 - International Resource Identifiers (IRIs)</span></span>  
  
## <a name="appendix-i---uri-scheme-registration-template-for-ms-infopath-scheme"></a><span data-ttu-id="5ef95-454">APÉNDICE I: PLANTILLA DE REGISTRO DE ESQUEMA URI PARA ESQUEMA MS-INFOPATH</span><span class="sxs-lookup"><span data-stu-id="5ef95-454">APPENDIX I - URI SCHEME REGISTRATION TEMPLATE FOR MS-INFOPATH SCHEME</span></span>
<span data-ttu-id="5ef95-455"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="5ef95-455"></span></span>

###   <a name="i-3-uri-scheme-syntax"></a><span data-ttu-id="5ef95-p196">I-3. Sintaxis de esquema URI</span><span class="sxs-lookup"><span data-stu-id="5ef95-p196">I-3. URI Scheme Syntax</span></span>

> <span data-ttu-id="5ef95-458">Esquema de Infopath = "ms-infopath:" open-for-edit-cmd | open-for-view-cmd</span><span class="sxs-lookup"><span data-stu-id="5ef95-458">Infopath Scheme = "ms-infopath:" open-for-edit-cmd | open-for-view-cmd</span></span>
    
> <span data-ttu-id="5ef95-459">open-for-edit-cmd = "ofe|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="5ef95-459">open-for-edit-cmd = "ofe|u|" document-uri</span></span>
    
> <span data-ttu-id="5ef95-460">open-for-view-cmd = "ofv|u|" document-uri</span><span class="sxs-lookup"><span data-stu-id="5ef95-460">open-for-view-cmd = "ofv|u|" document-uri</span></span>
    
> <span data-ttu-id="5ef95-461">document-uri = ubicación URI de documento para abrir</span><span class="sxs-lookup"><span data-stu-id="5ef95-461">document-uri = URI location of document to open</span></span>
    
### <a name="i-4-uri-scheme-semantics"></a><span data-ttu-id="5ef95-p197">I-4. Semántica de esquema URI</span><span class="sxs-lookup"><span data-stu-id="5ef95-p197">I-4. URI Scheme Semantics</span></span>

<span data-ttu-id="5ef95-p198">El esquema ms-infopath define una sintaxis URI para abrir o crear un documento de Microsoft Infopath. El esquema define dos comandos que sirven como instrucciones sobre qué se debe hacer con el documento de referencia. Los comandos son 1) open-for-edit-cmd (ofe), que indica a Visio que abra el documento en el URI especificado para la edición; y 2) open-for-view-cmd (ofv), que indica a Visio que abra el documento en el URI especificado en modo de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5ef95-p198">The ms-infopath scheme defines a URI syntax for opening or creating a Microsoft Infopath document. The scheme defines two commands that serve as instructions regarding what should be done with the referenced document. The commands are 1) open-for-edit-cmd (ofe), which instructs Visio to open the document at the specified URI for editing; and 2) open-for-view-cmd (ofv), which instructs Visio to open the document at the specified URI in a read-only mode.</span></span>
  
### <a name="i-5-applicationsprotocols-that-use-the-ms-infopath-uri-scheme"></a><span data-ttu-id="5ef95-p199">I-5. Aplicaciones/protocolos que usan el esquema URI ms-infopath</span><span class="sxs-lookup"><span data-stu-id="5ef95-p199">I-5. Applications/Protocols that use the ms-infopath URI Scheme</span></span>

<span data-ttu-id="5ef95-p200">Microsoft Office 2013 usa el esquema URI ms-infopath para invocar Microsoft Infopath 2013 desde páginas web. Microsoft SharePoint 2013 usa URI ms-infopath como vínculos a documentos de Infopath almacenados en bibliotecas de documentos de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="5ef95-p200">The ms-infopath URI Scheme is used by Microsoft Office 2013 to invoke Microsoft Infopath 2013 from web pages. Microsoft SharePoint 2013 uses ms-infopath URIs as links to Infopath documents stored in SharePoint document libraries.</span></span>
  
### <a name="i-6-interoperability-considerations"></a><span data-ttu-id="5ef95-p201">I-6. Consideraciones de interoperabilidad</span><span class="sxs-lookup"><span data-stu-id="5ef95-p201">I-6. Interoperability Considerations</span></span>

<span data-ttu-id="5ef95-p202">Tenga en cuenta que la barra vertical que se usa como delimitador de esta especificación no se encuentra entre los caracteres identificados en la sección 2.2 de RFC 3986 porque está reservado para uso potencial como delimitadores. Esto se hace intencionalmente para maximizar el conjunto de caracteres que el argumento de comando URI puede admitir sin necesidad de codificar los caracteres con porcentaje.</span><span class="sxs-lookup"><span data-stu-id="5ef95-p202">Note that the vertical bar used as a delimiter in this specification is not among those characters identified in section 2.2 of RFC 3986 as reserved for potential use as delimiters. This is done intentionally to maximize the set of characters the URI command argument can support without a need to percent-encode those characters.</span></span>
  
<span data-ttu-id="5ef95-475">Dentro de los segmentos < *argumento-comando*  > los caracteres reservados RFC 3986 ":" y "/" forman parte de los datos del argumento, no los delimitadores y por lo tanto, se incluyen sin secuencias de escape.</span><span class="sxs-lookup"><span data-stu-id="5ef95-475">Within < *command-argument*  > segments the RFC 3986 reserved characters ":" and "/" are part of the argument data, not delimiters, and are therefore included unescaped.</span></span> 
  
### <a name="i-7-security-considerations"></a><span data-ttu-id="5ef95-p203">I-7. Consideraciones de seguridad</span><span class="sxs-lookup"><span data-stu-id="5ef95-p203">I-7. Security Considerations</span></span>

<span data-ttu-id="5ef95-p204">En sistemas que tienen controladores registrados para reconocer y actuar en URI ms-infopath, al hacer clic en un vínculo a un URI ms-infopath, la aplicación registrada se iniciará, con instrucciones de que la aplicación intente abrir un documento en el URI especificado. Las aplicaciones que se registran para procesar URI ms-infopath deben implementar protecciones para protegerse contra la apertura de documentos desde sistemas remotos que no son de confianza y que pueden incluir código malintencionado.</span><span class="sxs-lookup"><span data-stu-id="5ef95-p204">On systems that have registered handlers to recognize and act on ms-infopath URIs, clicking on a link to an ms-infopath URI will cause the registered application to be launched, with instructions to the application to attempt to open a document at the specified URI. Applications registering to process ms-infopath URIs should implement protections to guard against opening documents from untrusted remote systems that may include malicious code.</span></span>
  
### <a name="i-8-references"></a><span data-ttu-id="5ef95-p205">I-8. Referencias</span><span class="sxs-lookup"><span data-stu-id="5ef95-p205">I-8. References</span></span>

<span data-ttu-id="5ef95-482">RFC 3987: Identificadores de recursos internacionales (IRI)</span><span class="sxs-lookup"><span data-stu-id="5ef95-482">RFC 3987 - International Resource Identifiers (IRIs)</span></span>  
  

