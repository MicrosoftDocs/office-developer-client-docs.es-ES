---
title: Entradas de propiedades en las secciones de servicios de mensaje MapiSvc. inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 714f99e2-80fc-4785-b707-611d8a6c229f
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: ad2732f2f8dba4f506318a1b6faefb617a60584a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428000"
---
# <a name="property-entries-in-mapisvcinf-message-service-sections"></a><span data-ttu-id="889d0-103">Entradas de propiedades en las secciones de servicios de mensaje MapiSvc. inf</span><span class="sxs-lookup"><span data-stu-id="889d0-103">Property Entries in MapiSvc.inf Message Service Sections</span></span>

  
  
<span data-ttu-id="889d0-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="889d0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="889d0-105">Las entradas que establecen propiedades utilizan este formato:</span><span class="sxs-lookup"><span data-stu-id="889d0-105">Entries that set properties use this format:</span></span>
  
 <span data-ttu-id="889d0-106">**etiqueta de propiedad** **=** valor de la propiedad</span><span class="sxs-lookup"><span data-stu-id="889d0-106">**property tag** **=** property value</span></span> 
  
<span data-ttu-id="889d0-107">La etiqueta de propiedad puede ser una etiqueta de propiedad MAPI estándar si los datos de configuración representan una de las propiedades predefinidas por MAPI, o una etiqueta no estándar si los datos no representan una propiedad MAPI.</span><span class="sxs-lookup"><span data-stu-id="889d0-107">The property tag can be a standard MAPI property tag if the configuration data represents one of the properties predefined by MAPI, or a nonstandard tag if the data does not represent a MAPI property.</span></span> <span data-ttu-id="889d0-108">La etiqueta no estándar se realiza combinando el valor de un identificador de propiedad con un tipo de propiedad.</span><span class="sxs-lookup"><span data-stu-id="889d0-108">The nonstandard tag is made by combining the value for a property identifier with a property type.</span></span> <span data-ttu-id="889d0-109">El resultado es un número hexadecimal de 8 dígitos.</span><span class="sxs-lookup"><span data-stu-id="889d0-109">The result is an 8 digit hexadecimal number.</span></span> <span data-ttu-id="889d0-110">El valor de la propiedad puede ser cualquiera que sea lógico para la etiqueta de propiedad.</span><span class="sxs-lookup"><span data-stu-id="889d0-110">The property value can be whatever makes sense for the property tag.</span></span> 
  
<span data-ttu-id="889d0-111">Las secciones del servicio de mensajes pueden contener una variedad de entradas que dependen del servicio de mensajes que se está configurando.</span><span class="sxs-lookup"><span data-stu-id="889d0-111">Message service sections can contain a variety of entries depending on the message service being configured.</span></span> <span data-ttu-id="889d0-112">Las siguientes propiedades MAPI se suelen incluir en una sección de servicios de mensajes en el formato enumerado:</span><span class="sxs-lookup"><span data-stu-id="889d0-112">The following MAPI properties are typically included in a message services section in the listed format:</span></span>
  
 <span data-ttu-id="889d0-113">\*\*\*\* =  _Cadena_ PR_DISPLAY_NAME</span><span class="sxs-lookup"><span data-stu-id="889d0-113">**PR_DISPLAY_NAME** =  _string_</span></span>
  
 <span data-ttu-id="889d0-114">**PR_SERVICE_DLL_NAME** =  _nombre del archivo dll_</span><span class="sxs-lookup"><span data-stu-id="889d0-114">**PR_SERVICE_DLL_NAME** =  _name of DLL file_</span></span>
  
 <span data-ttu-id="889d0-115">**PR_SERVICE_ENTRY_NAME** =  _nombre de función de punto de entrada_</span><span class="sxs-lookup"><span data-stu-id="889d0-115">**PR_SERVICE_ENTRY_NAME** =  _name of entry point function_</span></span>
  
 <span data-ttu-id="889d0-116">\*\*\*\* =  _Lista de archivos de_ PR_SERVICE_SUPPORT_FILES</span><span class="sxs-lookup"><span data-stu-id="889d0-116">**PR_SERVICE_SUPPORT_FILES** =  _list of files_</span></span>
  
 <span data-ttu-id="889d0-117">\*\*\*\* =  _Lista de archivos de_ PR_SERVICE_DELETE_FILES</span><span class="sxs-lookup"><span data-stu-id="889d0-117">**PR_SERVICE_DELETE_FILES** =  _list of files_</span></span>
  
 <span data-ttu-id="889d0-118">\*\*\*\* =  _Máscara_ de PR_RESOURCE_FLAGS</span><span class="sxs-lookup"><span data-stu-id="889d0-118">**PR_RESOURCE_FLAGS** =  _bitmask_</span></span>
  
<span data-ttu-id="889d0-119">La cadena **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) es el nombre del servicio de mensajes que se muestra en la interfaz de usuario, el nombre que el usuario asocia con el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="889d0-119">The **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) string is the name of the message service that is shown in the user interface, the name that the user associates with the message service.</span></span> <span data-ttu-id="889d0-120">El nombre para mostrar es una entrada opcional en MAPISVC. inf.</span><span class="sxs-lookup"><span data-stu-id="889d0-120">The display name is an optional entry in mapisvc.inf.</span></span> <span data-ttu-id="889d0-121">A veces, el nombre para mostrar constará de dos partes; una parte asignada por el servicio de mensajes y una parte asignada por el usuario.</span><span class="sxs-lookup"><span data-stu-id="889d0-121">Sometimes the display name will be made up of two parts; a part assigned by the message service and a part assigned by the user.</span></span> <span data-ttu-id="889d0-122">Si el usuario es responsable de asignar una de las partes, normalmente se controla con un cuadro de diálogo especial conocido como una hoja de propiedades suministrada por el servicio de mensajes bajo el control de una aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="889d0-122">If the user is responsible for assigning one of the parts, this is typically handled with a special dialog box known as a property sheet supplied by the message service under the control of a client application.</span></span> 
  
<span data-ttu-id="889d0-123">La información proporcionada para la entrada **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) es el nombre de la dll que contiene el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="889d0-123">The information provided for the **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) entry is the name of the DLL that contains the message service.</span></span> <span data-ttu-id="889d0-124">La información proporcionada para la entrada **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) es el nombre de la función de punto de entrada dentro de la dll que MAPI llama para configurar el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="889d0-124">The information provided for the **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) entry is the name of the entry point function within that DLL that MAPI calls to configure the message service.</span></span> 
  
<span data-ttu-id="889d0-125">Los archivos que aparecen en la entrada **PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md)) son archivos que se deben instalar con el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="889d0-125">The files listed in the **PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md)) entry are files that must be installed with the message service.</span></span> <span data-ttu-id="889d0-126">Del mismo modo, los archivos de la entrada **PR_SERVICE_DELETE_FILES** ([PidTagServiceDeleteFiles](pidtagservicedeletefiles-canonical-property.md)) deben quitarse cuando se quita el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="889d0-126">Likewise, the files in the **PR_SERVICE_DELETE_FILES** ([PidTagServiceDeleteFiles](pidtagservicedeletefiles-canonical-property.md)) entry must be removed when the message service is removed.</span></span> 
  
<span data-ttu-id="889d0-127">La entrada **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) es una colección de opciones definidas para el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="889d0-127">The **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) entry is a collection of options defined for the message service.</span></span> <span data-ttu-id="889d0-128">Por ejemplo, el bit SERVICE_SINGLE_COPY se establece cuando el servicio de mensajes solo puede aparecer una vez en un perfil determinado.</span><span class="sxs-lookup"><span data-stu-id="889d0-128">For example, the SERVICE_SINGLE_COPY bit is set when the message service can only appear once in a given profile.</span></span> <span data-ttu-id="889d0-129">El bit SERVICE_NO_PRIMARY_IDENTITY se establece si el servicio de mensajes no proporciona información de identidad.</span><span class="sxs-lookup"><span data-stu-id="889d0-129">The SERVICE_NO_PRIMARY_IDENTITY bit is set if the message service does not provide identity information.</span></span> 
  
<span data-ttu-id="889d0-130">A continuación se muestran dos ejemplos de entradas de propiedades no estándar.</span><span class="sxs-lookup"><span data-stu-id="889d0-130">Two examples of nonstandard property entries follow.</span></span> <span data-ttu-id="889d0-131">La primera entrada especifica la ruta de acceso al archivo usado por la libreta de direcciones predeterminada como valor de la propiedad; la segunda entrada especifica un valor de propiedad numérica.</span><span class="sxs-lookup"><span data-stu-id="889d0-131">The first entry specifies the path to the file used by the Default Address Book as the property value; the second entry specifies a numeric property value.</span></span> <span data-ttu-id="889d0-132">Ambas entradas tienen significado específico del servicio de mensajes AB.</span><span class="sxs-lookup"><span data-stu-id="889d0-132">Both entries have meaning specific to the AB message service.</span></span>
  
```cpp
6600001e=full path to file
66040003=integer

```


