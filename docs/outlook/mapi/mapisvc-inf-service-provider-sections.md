---
title: Secciones del proveedor de servicios MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ab17dcf2-409b-4a57-9cc4-5794f995cd3e
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: ea192ec6356cc3b929bf8379567144d3a54223f2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405565"
---
# <a name="mapisvcinf-service-provider-sections"></a><span data-ttu-id="da112-103">Secciones del proveedor de servicios MapiSvc.inf</span><span class="sxs-lookup"><span data-stu-id="da112-103">MapiSvc.inf Service Provider Sections</span></span>

<span data-ttu-id="da112-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="da112-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="da112-105">Mapisvc.inf incluye una sección de proveedor de servicios  para cada una de las entradas enumeradas en la entrada Proveedores de la sección servicios de mensajes anterior.</span><span class="sxs-lookup"><span data-stu-id="da112-105">Mapisvc.inf includes one service provider section for each of the entries listed in the **Providers** entry in the preceding message services section.</span></span> <span data-ttu-id="da112-106">**Las** secciones del proveedor de servicios son similares a las secciones de servicio de mensajes en las que ambos tipos de secciones contienen entradas en este formato:</span><span class="sxs-lookup"><span data-stu-id="da112-106">**Service** provider sections are similar to message service sections in that both types of sections contain entries in this format:</span></span> 
  
<span data-ttu-id="da112-107">**etiqueta de propiedad** = valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="da112-107">**property tag** = property value</span></span> 
  
<span data-ttu-id="da112-108">Sin embargo, las secciones del proveedor de servicios y las secciones de servicio de mensajes difieren en que dichas entradas de propiedad son el único tipo de entrada incluido en las secciones del proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="da112-108">However, service provider sections and message service sections differ in that such property entries are the only type of entry included in service provider sections.</span></span> <span data-ttu-id="da112-109">No puede haber secciones adicionales ni vinculadas para los proveedores de servicios; toda la información del proveedor de servicios debe estar incluida en una sección.</span><span class="sxs-lookup"><span data-stu-id="da112-109">There can be no additional or linked sections for service providers; all service provider information must be contained within the one section.</span></span> 
  
<span data-ttu-id="da112-110">Algunas de las propiedades establecidas en las secciones de servicio de mensajes también se establecen en las secciones del proveedor de servicios porque estas propiedades tienen sentido para ambas.</span><span class="sxs-lookup"><span data-stu-id="da112-110">Some of the properties set in message service sections are also set in service provider sections because these properties make sense for both.</span></span> <span data-ttu-id="da112-111">La **PR_DISPLAY_NAME** es un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="da112-111">The **PR_DISPLAY_NAME** property is an example.</span></span> <span data-ttu-id="da112-112">Tanto los proveedores de servicios como los servicios de mensajes tienen un nombre que se usa para mostrarse en la interfaz de usuario de configuración.</span><span class="sxs-lookup"><span data-stu-id="da112-112">Both service providers and message services have a name that is used for display in the configuration user interface.</span></span> <span data-ttu-id="da112-113">Según el proveedor de servicios, ese nombre puede ser o no el mismo.</span><span class="sxs-lookup"><span data-stu-id="da112-113">Depending on the service provider, that name may or may not be the same.</span></span> <span data-ttu-id="da112-114">Otras propiedades son específicas de los proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="da112-114">Other properties are specific to service providers.</span></span> 
  
<span data-ttu-id="da112-115">Las secciones típicas del proveedor de servicios incluyen las siguientes entradas, todas ellas necesarias:</span><span class="sxs-lookup"><span data-stu-id="da112-115">Typical service provider sections include the following entries, all of which are required:</span></span>
  
<span data-ttu-id="da112-116">**PR_DISPLAY_NAME**  =   _string_</span><span class="sxs-lookup"><span data-stu-id="da112-116">**PR_DISPLAY_NAME** =  _string_</span></span>
  
<span data-ttu-id="da112-117">**PR_PROVIDER_DISPLAY**  =   _string_</span><span class="sxs-lookup"><span data-stu-id="da112-117">**PR_PROVIDER_DISPLAY** =  _string_</span></span>
  
<span data-ttu-id="da112-118">**PR_PROVIDER_DLL_NAME**  =   _nombre del archivo DLL_</span><span class="sxs-lookup"><span data-stu-id="da112-118">**PR_PROVIDER_DLL_NAME** =  _name of DLL file_</span></span>
  
<span data-ttu-id="da112-119">**PR_RESOURCE_TYPE**  =   _long_</span><span class="sxs-lookup"><span data-stu-id="da112-119">**PR_RESOURCE_TYPE** =  _long_</span></span>
  
<span data-ttu-id="da112-120">**PR_RESOURCE_FLAGS**  =   _máscara de bits_</span><span class="sxs-lookup"><span data-stu-id="da112-120">**PR_RESOURCE_FLAGS** =  _bitmask_</span></span>
  
<span data-ttu-id="da112-121">La **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) es similar a **PR_SERVICE_DLL_NAME**; indica el nombre de archivo de la DLL que contiene el proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="da112-121">The **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) entry is similar to **PR_SERVICE_DLL_NAME**; it indicates the filename for the DLL that contains the service provider.</span></span> <span data-ttu-id="da112-122">El código de servicio de mensajes puede almacenarse con uno de sus proveedores de servicios en el mismo archivo DLL o existir como un ARCHIVO DLL independiente.</span><span class="sxs-lookup"><span data-stu-id="da112-122">Message service code may be stored with one of its service providers in the same DLL file or exist as a separate DLL.</span></span> <span data-ttu-id="da112-123">Tenga en cuenta que no se incluye ningún sufijo en la entrada independientemente de la plataforma de destino; MAPI se encarga de agregar un sufijo si es necesario.</span><span class="sxs-lookup"><span data-stu-id="da112-123">Note that no suffix is included in the entry regardless of the target platform; MAPI takes care of adding a suffix if necessary.</span></span> 
  
<span data-ttu-id="da112-124">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) entrada representa el tipo de proveedor de servicios; los proveedores de servicios lo establecen en la constante predefinida adecuada.</span><span class="sxs-lookup"><span data-stu-id="da112-124">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) entry represents the type of service provider; service providers set it to the appropriate predefined constant.</span></span> <span data-ttu-id="da112-125">Los valores válidos MAPI_STORE_PROVIDER, MAPI_TRANSPORT_PROVIDER y MAPI_AB_PROVIDER.</span><span class="sxs-lookup"><span data-stu-id="da112-125">Valid values include MAPI_STORE_PROVIDER, MAPI_TRANSPORT_PROVIDER, and MAPI_AB_PROVIDER.</span></span>
  
<span data-ttu-id="da112-126">Otra entrada de propiedad que se aplica tanto a los servicios de mensajes como a los proveedores **de** servicios, la PR_RESOURCE_FLAGS ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) indica opciones.</span><span class="sxs-lookup"><span data-stu-id="da112-126">Another property entry that applies to both message services and service providers, the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) entry indicates options.</span></span> <span data-ttu-id="da112-127">La configuración de esta entrada de propiedad puede variar según el proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="da112-127">The settings for this property entry can differ depending on the service provider.</span></span> <span data-ttu-id="da112-128">Por ejemplo, algunos proveedores de almacén de mensajes pueden establecer **PR_RESOURCE_FLAGS** en STATUS_NO_DEFAULT_STORE si nunca pueden funcionar como el almacén de mensajes predeterminado.</span><span class="sxs-lookup"><span data-stu-id="da112-128">For example, some message store providers might set **PR_RESOURCE_FLAGS** to STATUS_NO_DEFAULT_STORE if they can never operate as the default message store.</span></span> 
  
<span data-ttu-id="da112-129">A continuación se muestran tres ejemplos de secciones de proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="da112-129">Three examples of service provider sections follow.</span></span> <span data-ttu-id="da112-130">La **sección [Proveedor AB]** es la sección proveedor de servicios para el servicio de libreta de direcciones predeterminada.</span><span class="sxs-lookup"><span data-stu-id="da112-130">The **[AB Provider]** section is the service provider section for the Default Address Book service.</span></span> <span data-ttu-id="da112-131">Las **secciones [MsgService Prov1]** y **[MsgService Prov2]** pertenecen a Mi propio servicio; la primera es una sección de proveedor de libreta de direcciones y la segunda es una sección de proveedor de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="da112-131">The **[MsgService Prov1]** and **[MsgService Prov2]** sections belong to My Own Service; the first is an address-book provider section and the second is a message-store provider section.</span></span> 
  
```cpp
[AB Provider]
PR_DISPLAY_NAME=Default Address Book
PR_PROVIDER_DISPLAY=Default Address Book
PR_PROVIDER_DLL_NAME=AB.DLL
PR_RESOURCE_TYPE=MAPI_AB_PROVIDER
6600001e=C:\WINNT35\System32\DEFAB.TXT
[MsgService Prov1]
PR_DISPLAY_NAME=My Own Service
PR_PROVIDER_DISPLAY=My Own Address Book
PR_PROVIDER_DLL_NAME=MYXXX.DLL
PR_RESOURCE_TYPE=MAPI_AB_PROVIDER
[MsgService Prov2]
PR_DISPLAY_NAME=My Folders
PR_PROVIDER_DISPLAY=My Own Message Store
PR_RESOURCE_TYPE=MAPI_STORE_PROVIDER
PR_PROVIDER_DLL_NAME=MYZZZ.DLL
PR_RESOURCE_FLAGS=STATUS_NO_DEFAULT_STORE
66060003=00000000
66030003=00000000
34140102=78b2fa70aff711cd9bc800aa002fc45a
66090003=06000000
660A0003=03000000

```


