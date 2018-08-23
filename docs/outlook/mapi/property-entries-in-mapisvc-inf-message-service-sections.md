---
title: Entradas de las propiedades de las secciones de servicios de mensaje MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 714f99e2-80fc-4785-b707-611d8a6c229f
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 038c13d24f3d797f7a4f8f9b7692240ce8004b74
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580337"
---
# <a name="property-entries-in-mapisvcinf-message-service-sections"></a><span data-ttu-id="4a0ba-103">Entradas de las propiedades de las secciones de servicios de mensaje MapiSvc.inf</span><span class="sxs-lookup"><span data-stu-id="4a0ba-103">Property Entries in MapiSvc.inf Message Service Sections</span></span>

  
  
<span data-ttu-id="4a0ba-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4a0ba-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4a0ba-105">Las entradas que establecer las propiedades de usar este formato:</span><span class="sxs-lookup"><span data-stu-id="4a0ba-105">Entries that set properties use this format:</span></span>
  
 <span data-ttu-id="4a0ba-106">**etiqueta (propiedad)** **=** valor de la propiedad</span><span class="sxs-lookup"><span data-stu-id="4a0ba-106">**property tag** **=** property value</span></span> 
  
<span data-ttu-id="4a0ba-107">La etiqueta de propiedad puede ser una etiqueta de propiedad MAPI estándar si los datos de configuración representan una de las propiedades predeterminadas de MAPI o una etiqueta no estándar si los datos no representan una propiedad MAPI.</span><span class="sxs-lookup"><span data-stu-id="4a0ba-107">The property tag can be a standard MAPI property tag if the configuration data represents one of the properties predefined by MAPI, or a nonstandard tag if the data does not represent a MAPI property.</span></span> <span data-ttu-id="4a0ba-108">La etiqueta no estándar se realiza mediante la combinación del valor de un identificador de propiedad con un tipo de propiedad.</span><span class="sxs-lookup"><span data-stu-id="4a0ba-108">The nonstandard tag is made by combining the value for a property identifier with a property type.</span></span> <span data-ttu-id="4a0ba-109">El resultado es un número hexadecimal de 8 dígitos.</span><span class="sxs-lookup"><span data-stu-id="4a0ba-109">The result is an 8 digit hexadecimal number.</span></span> <span data-ttu-id="4a0ba-110">El valor de la propiedad puede ser todo lo que tiene sentido para la etiqueta de propiedad.</span><span class="sxs-lookup"><span data-stu-id="4a0ba-110">The property value can be whatever makes sense for the property tag.</span></span> 
  
<span data-ttu-id="4a0ba-111">Las secciones de servicio de mensaje pueden contener una gran variedad de entradas de función que se está configurando el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="4a0ba-111">Message service sections can contain a variety of entries depending on the message service being configured.</span></span> <span data-ttu-id="4a0ba-112">Normalmente, se incluyen las siguientes propiedades MAPI en una sección de servicios de mensaje en el formato de lista:</span><span class="sxs-lookup"><span data-stu-id="4a0ba-112">The following MAPI properties are typically included in a message services section in the listed format:</span></span>
  
 <span data-ttu-id="4a0ba-113">**PR_DISPLAY_NAME** =  _cadena_</span><span class="sxs-lookup"><span data-stu-id="4a0ba-113">**PR_DISPLAY_NAME** =  _string_</span></span>
  
 <span data-ttu-id="4a0ba-114">**PR_SERVICE_DLL_NAME** =  _nombre del archivo DLL_</span><span class="sxs-lookup"><span data-stu-id="4a0ba-114">**PR_SERVICE_DLL_NAME** =  _name of DLL file_</span></span>
  
 <span data-ttu-id="4a0ba-115">**PR_SERVICE_ENTRY_NAME** =  _nombre de función de punto de entrada_</span><span class="sxs-lookup"><span data-stu-id="4a0ba-115">**PR_SERVICE_ENTRY_NAME** =  _name of entry point function_</span></span>
  
 <span data-ttu-id="4a0ba-116">**PR_SERVICE_SUPPORT_FILES** =  _lista de archivos_</span><span class="sxs-lookup"><span data-stu-id="4a0ba-116">**PR_SERVICE_SUPPORT_FILES** =  _list of files_</span></span>
  
 <span data-ttu-id="4a0ba-117">**PR_SERVICE_DELETE_FILES** =  _lista de archivos_</span><span class="sxs-lookup"><span data-stu-id="4a0ba-117">**PR_SERVICE_DELETE_FILES** =  _list of files_</span></span>
  
 <span data-ttu-id="4a0ba-118">**PR_RESOURCE_FLAGS** =  _máscara de bits_</span><span class="sxs-lookup"><span data-stu-id="4a0ba-118">**PR_RESOURCE_FLAGS** =  _bitmask_</span></span>
  
<span data-ttu-id="4a0ba-119">La cadena de **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) es el nombre del servicio de mensaje que se muestra en la interfaz de usuario, el nombre que el usuario se asocia con el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="4a0ba-119">The **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) string is the name of the message service that is shown in the user interface, the name that the user associates with the message service.</span></span> <span data-ttu-id="4a0ba-120">El nombre para mostrar es una entrada opcional en mapisvc.inf.</span><span class="sxs-lookup"><span data-stu-id="4a0ba-120">The display name is an optional entry in mapisvc.inf.</span></span> <span data-ttu-id="4a0ba-121">En ocasiones, el nombre para mostrar se constar de dos partes; un elemento asignado por el servicio de mensajes y un elemento asignado por el usuario.</span><span class="sxs-lookup"><span data-stu-id="4a0ba-121">Sometimes the display name will be made up of two parts; a part assigned by the message service and a part assigned by the user.</span></span> <span data-ttu-id="4a0ba-122">Si el usuario es responsable de asignar uno de los elementos, normalmente esto se controla con un cuadro de diálogo especial conocido como una hoja de propiedades suministrada por el servicio de mensajes bajo el control de una aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="4a0ba-122">If the user is responsible for assigning one of the parts, this is typically handled with a special dialog box known as a property sheet supplied by the message service under the control of a client application.</span></span> 
  
<span data-ttu-id="4a0ba-123">La información proporcionada para la entrada de **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) es el nombre del archivo DLL que contiene el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="4a0ba-123">The information provided for the **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) entry is the name of the DLL that contains the message service.</span></span> <span data-ttu-id="4a0ba-124">La información proporcionada para la entrada de **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) es el nombre de la función de punto de entrada dentro de ese archivo DLL que llama MAPI para configurar el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="4a0ba-124">The information provided for the **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) entry is the name of the entry point function within that DLL that MAPI calls to configure the message service.</span></span> 
  
<span data-ttu-id="4a0ba-125">Los archivos que aparecen en la entrada de **PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md)) son archivos que deben estar instalados con el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="4a0ba-125">The files listed in the **PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md)) entry are files that must be installed with the message service.</span></span> <span data-ttu-id="4a0ba-126">Del mismo modo, se deben quitar los archivos en la entrada de **PR_SERVICE_DELETE_FILES** ([PidTagServiceDeleteFiles](pidtagservicedeletefiles-canonical-property.md)) cuando se quita el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="4a0ba-126">Likewise, the files in the **PR_SERVICE_DELETE_FILES** ([PidTagServiceDeleteFiles](pidtagservicedeletefiles-canonical-property.md)) entry must be removed when the message service is removed.</span></span> 
  
<span data-ttu-id="4a0ba-127">La entrada **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) es una colección de opciones definida para el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="4a0ba-127">The **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) entry is a collection of options defined for the message service.</span></span> <span data-ttu-id="4a0ba-128">Por ejemplo, se establece el bit SERVICE_SINGLE_COPY cuando el servicio de mensajes sólo puede aparecer una vez en un perfil dado.</span><span class="sxs-lookup"><span data-stu-id="4a0ba-128">For example, the SERVICE_SINGLE_COPY bit is set when the message service can only appear once in a given profile.</span></span> <span data-ttu-id="4a0ba-129">Si el servicio de mensajes no proporciona información de identidad, se establece el bit SERVICE_NO_PRIMARY_IDENTITY.</span><span class="sxs-lookup"><span data-stu-id="4a0ba-129">The SERVICE_NO_PRIMARY_IDENTITY bit is set if the message service does not provide identity information.</span></span> 
  
<span data-ttu-id="4a0ba-130">Siguen dos ejemplos de entradas de la propiedad no estándar.</span><span class="sxs-lookup"><span data-stu-id="4a0ba-130">Two examples of nonstandard property entries follow.</span></span> <span data-ttu-id="4a0ba-131">La primera entrada especifica la ruta de acceso para el archivo usado por la libreta de direcciones predeterminada como el valor de la propiedad; la segunda entrada especifica un valor numérico (propiedad).</span><span class="sxs-lookup"><span data-stu-id="4a0ba-131">The first entry specifies the path to the file used by the Default Address Book as the property value; the second entry specifies a numeric property value.</span></span> <span data-ttu-id="4a0ba-132">Ambas entradas tienen un significado específico para el servicio de mensajes AB.</span><span class="sxs-lookup"><span data-stu-id="4a0ba-132">Both entries have meaning specific to the AB message service.</span></span>
  
```cpp
6600001e=full path to file
66040003=integer

```


