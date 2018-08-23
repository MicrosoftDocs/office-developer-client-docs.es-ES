---
title: Propiedad canónica PidTagProfileServerVersion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5d41a536-81ff-733c-2fd7-460798e057c8
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 79b6461ca4a796b292b86f0f3bdbd8a39ad65863
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575682"
---
# <a name="pidtagprofileserverversion-canonical-property"></a><span data-ttu-id="e16f6-103">Propiedad canónica PidTagProfileServerVersion</span><span class="sxs-lookup"><span data-stu-id="e16f6-103">PidTagProfileServerVersion Canonical Property</span></span>

  
  
<span data-ttu-id="e16f6-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e16f6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e16f6-105">Especifica información acerca de la versión de Microsoft Exchange Server a la que están conectadas cuentas en un perfil de Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="e16f6-105">Specifies information about the version of Microsoft Exchange Server to which accounts in a Microsoft Outlook profile are connected.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="e16f6-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="e16f6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e16f6-107">PR_PROFILE_SERVER_VERSION</span><span class="sxs-lookup"><span data-stu-id="e16f6-107">PR_PROFILE_SERVER_VERSION</span></span>  <br/> |
|<span data-ttu-id="e16f6-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="e16f6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e16f6-109">0x661B</span><span class="sxs-lookup"><span data-stu-id="e16f6-109">0x661B</span></span>  <br/> |
|<span data-ttu-id="e16f6-110">Tipo de propiedad:</span><span class="sxs-lookup"><span data-stu-id="e16f6-110">Property type:</span></span>  <br/> |<span data-ttu-id="e16f6-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e16f6-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="e16f6-112">Área:</span><span class="sxs-lookup"><span data-stu-id="e16f6-112">Area:</span></span>  <br/> |<span data-ttu-id="e16f6-113">Configuración de perfiles de MAPI</span><span class="sxs-lookup"><span data-stu-id="e16f6-113">MAPI profile configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e16f6-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e16f6-114">Remarks</span></span>

<span data-ttu-id="e16f6-115">Un perfil puede especificar una o más cuentas que se conectan a un servidor de Exchange, pero deben estar conectados al mismo servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e16f6-115">A profile can specify one or more accounts that connect to an Exchange Server, but they must be connected to the same Exchange Server.</span></span>
  
<span data-ttu-id="e16f6-116">Versiones de Outlook anteriores a Microsoft Office Outlook 2007 pueden escribir en esta propiedad para almacenar información acerca de la versión de Exchange Server al que está conectado el perfil activo.</span><span class="sxs-lookup"><span data-stu-id="e16f6-116">Versions of Outlook earlier than Microsoft Office Outlook 2007 can write to this property to store information about the version of Exchange Server to which the active profile is connected.</span></span> <span data-ttu-id="e16f6-117">Sin embargo, el formato de la información de versión varía en función de las diferentes versiones de Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="e16f6-117">However, the format of the version information varies for different versions of Exchange Server.</span></span> <span data-ttu-id="e16f6-118">Por ejemplo, almacenes de Outlook en **PR_PROFILE_SERVER_VERSION** el valor decimal 6944 para representar a sólo los principales número de compilación en el identificador de versión de **6.5.6944.3** para Microsoft Exchange Server 2003.</span><span class="sxs-lookup"><span data-stu-id="e16f6-118">For example, Outlook stores in **PR_PROFILE_SERVER_VERSION** the decimal value 6944 to represent only the major build number in the version identifier of **6.5.6944.3** for Microsoft Exchange Server 2003.</span></span> <span data-ttu-id="e16f6-119">Para una conexión de Exchange 2007, Outlook almacena el número de versión principal y el mayor número de compilación en una representación hexadecimal concatenada de estos números en la propiedad.</span><span class="sxs-lookup"><span data-stu-id="e16f6-119">For an Exchange 2007 connection, Outlook stores the major version number and the major build number in a concatenated hexadecimal representation of these numbers in the property.</span></span> <span data-ttu-id="e16f6-120">Un identificador de versión de Exchange 2007 de **8.0.685.24** tiene un número de versión principal 8 y un número de versión de compilación principal 685 en decimal.</span><span class="sxs-lookup"><span data-stu-id="e16f6-120">An Exchange 2007 version identifier of **8.0.685.24** has a major version number 8 and a major build number 685 in decimal.</span></span> <span data-ttu-id="e16f6-121">Conversión de ambos números en hexadecimal, obtendrá 0 x 8 y 0x2AD.</span><span class="sxs-lookup"><span data-stu-id="e16f6-121">Converting both numbers to hexadecimal, you get 0x8 and 0x2AD.</span></span> <span data-ttu-id="e16f6-122">Concatenación de estos dos números, Outlook almacena el valor 0x82AD en **PR_PROFILE_SERVER_VERSION** en representación hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="e16f6-122">Concatenating these two numbers, Outlook stores the value 0x82AD in **PR_PROFILE_SERVER_VERSION** in hexadecimal representation.</span></span> 
  
<span data-ttu-id="e16f6-123">Outlook 2007 no leer o escribir en esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="e16f6-123">Outlook 2007 does not read or write to this property.</span></span> <span data-ttu-id="e16f6-124">Admite **[PR_PROFILE_SERVER_FULL_VERSION](pidtagprofileserverfullversion-canonical-property.md)**.</span><span class="sxs-lookup"><span data-stu-id="e16f6-124">It supports **[PR_PROFILE_SERVER_FULL_VERSION](pidtagprofileserverfullversion-canonical-property.md)**.</span></span> 
  
<span data-ttu-id="e16f6-125">Solo uno de **PR_PROFILE_SERVER_VERSION** o **PR_PROFILE_SERVER_FULL_VERSION** es probable que existan en un perfil, pero no hay ninguna garantía de que siempre existe alguna en un perfil.</span><span class="sxs-lookup"><span data-stu-id="e16f6-125">Only one of **PR_PROFILE_SERVER_VERSION** or **PR_PROFILE_SERVER_FULL_VERSION** is likely to exist in a profile, but there is no guarantee that either always exists in a profile.</span></span> <span data-ttu-id="e16f6-126">Outlook no se escribe en cualquiera de las propiedades hasta que se haya conectado correctamente al servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e16f6-126">Outlook does not write to either property until it has successfully connected to the Exchange Server.</span></span> 
  
<span data-ttu-id="e16f6-127">En el modelo de objetos de Outlook, puede usar la propiedad **ExchangeMailboxServerVersion** del objeto **NameSpace** para buscar la versión de Exchange Server en el que se hospeda el buzón activo.</span><span class="sxs-lookup"><span data-stu-id="e16f6-127">In the Outlook object model, you can use the **ExchangeMailboxServerVersion** property of the **NameSpace** object to find the version of Exchange Server on which the active mailbox is hosted.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e16f6-128">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e16f6-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e16f6-129">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="e16f6-129">Protocol specifications</span></span>

<span data-ttu-id="e16f6-130">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e16f6-130">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e16f6-131">Proporciona definiciones de conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="e16f6-131">Provides property set definitions.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e16f6-132">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="e16f6-132">Header files</span></span>

<span data-ttu-id="e16f6-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e16f6-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="e16f6-134">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="e16f6-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="e16f6-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e16f6-135">Mapitags.h</span></span>
  
> <span data-ttu-id="e16f6-136">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="e16f6-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e16f6-137">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="e16f6-137">See also</span></span>



[<span data-ttu-id="e16f6-138">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e16f6-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e16f6-139">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="e16f6-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e16f6-140">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="e16f6-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e16f6-141">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="e16f6-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

