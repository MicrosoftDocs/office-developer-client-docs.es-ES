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
ms.openlocfilehash: 84ff229e9914ec9074d61023873279b110fb606a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397642"
---
# <a name="pidtagprofileserverversion-canonical-property"></a><span data-ttu-id="66e85-103">Propiedad canónica PidTagProfileServerVersion</span><span class="sxs-lookup"><span data-stu-id="66e85-103">PidTagProfileServerVersion Canonical Property</span></span>

  
  
<span data-ttu-id="66e85-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="66e85-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="66e85-105">Especifica información acerca de la versión de Microsoft Exchange Server a la que están conectadas cuentas en un perfil de Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="66e85-105">Specifies information about the version of Microsoft Exchange Server to which accounts in a Microsoft Outlook profile are connected.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="66e85-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="66e85-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="66e85-107">PR_PROFILE_SERVER_VERSION</span><span class="sxs-lookup"><span data-stu-id="66e85-107">PR_PROFILE_SERVER_VERSION</span></span>  <br/> |
|<span data-ttu-id="66e85-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="66e85-108">Identifier:</span></span>  <br/> |<span data-ttu-id="66e85-109">0x661B</span><span class="sxs-lookup"><span data-stu-id="66e85-109">0x661B</span></span>  <br/> |
|<span data-ttu-id="66e85-110">Tipo de propiedad:</span><span class="sxs-lookup"><span data-stu-id="66e85-110">Property type:</span></span>  <br/> |<span data-ttu-id="66e85-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="66e85-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="66e85-112">Área:</span><span class="sxs-lookup"><span data-stu-id="66e85-112">Area:</span></span>  <br/> |<span data-ttu-id="66e85-113">Configuración de perfiles de MAPI</span><span class="sxs-lookup"><span data-stu-id="66e85-113">MAPI profile configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="66e85-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="66e85-114">Remarks</span></span>

<span data-ttu-id="66e85-115">Un perfil puede especificar una o más cuentas que se conectan a un servidor de Exchange, pero deben estar conectados al mismo servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="66e85-115">A profile can specify one or more accounts that connect to an Exchange Server, but they must be connected to the same Exchange Server.</span></span>
  
<span data-ttu-id="66e85-116">Versiones de Outlook anteriores a Microsoft Office Outlook 2007 pueden escribir en esta propiedad para almacenar información acerca de la versión de Exchange Server al que está conectado el perfil activo.</span><span class="sxs-lookup"><span data-stu-id="66e85-116">Versions of Outlook earlier than Microsoft Office Outlook 2007 can write to this property to store information about the version of Exchange Server to which the active profile is connected.</span></span> <span data-ttu-id="66e85-117">Sin embargo, el formato de la información de versión varía en función de las diferentes versiones de Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="66e85-117">However, the format of the version information varies for different versions of Exchange Server.</span></span> <span data-ttu-id="66e85-118">Por ejemplo, almacenes de Outlook en **PR_PROFILE_SERVER_VERSION** el valor decimal 6944 para representar a sólo los principales número de compilación en el identificador de versión de **6.5.6944.3** para Microsoft Exchange Server 2003.</span><span class="sxs-lookup"><span data-stu-id="66e85-118">For example, Outlook stores in **PR_PROFILE_SERVER_VERSION** the decimal value 6944 to represent only the major build number in the version identifier of **6.5.6944.3** for Microsoft Exchange Server 2003.</span></span> <span data-ttu-id="66e85-119">Para una conexión de Exchange 2007, Outlook almacena el número de versión principal y el mayor número de compilación en una representación hexadecimal concatenada de estos números en la propiedad.</span><span class="sxs-lookup"><span data-stu-id="66e85-119">For an Exchange 2007 connection, Outlook stores the major version number and the major build number in a concatenated hexadecimal representation of these numbers in the property.</span></span> <span data-ttu-id="66e85-120">Un identificador de versión de Exchange 2007 de **8.0.685.24** tiene un número de versión principal 8 y un número de versión de compilación principal 685 en decimal.</span><span class="sxs-lookup"><span data-stu-id="66e85-120">An Exchange 2007 version identifier of **8.0.685.24** has a major version number 8 and a major build number 685 in decimal.</span></span> <span data-ttu-id="66e85-121">Conversión de ambos números en hexadecimal, obtendrá 0 x 8 y 0x2AD.</span><span class="sxs-lookup"><span data-stu-id="66e85-121">Converting both numbers to hexadecimal, you get 0x8 and 0x2AD.</span></span> <span data-ttu-id="66e85-122">Concatenación de estos dos números, Outlook almacena el valor 0x82AD en **PR_PROFILE_SERVER_VERSION** en representación hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="66e85-122">Concatenating these two numbers, Outlook stores the value 0x82AD in **PR_PROFILE_SERVER_VERSION** in hexadecimal representation.</span></span> 
  
<span data-ttu-id="66e85-123">Outlook 2007 no leer o escribir en esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="66e85-123">Outlook 2007 does not read or write to this property.</span></span> <span data-ttu-id="66e85-124">Admite **[PR_PROFILE_SERVER_FULL_VERSION](pidtagprofileserverfullversion-canonical-property.md)**.</span><span class="sxs-lookup"><span data-stu-id="66e85-124">It supports **[PR_PROFILE_SERVER_FULL_VERSION](pidtagprofileserverfullversion-canonical-property.md)**.</span></span> 
  
<span data-ttu-id="66e85-125">Solo uno de **PR_PROFILE_SERVER_VERSION** o **PR_PROFILE_SERVER_FULL_VERSION** es probable que existan en un perfil, pero no hay ninguna garantía de que siempre existe alguna en un perfil.</span><span class="sxs-lookup"><span data-stu-id="66e85-125">Only one of **PR_PROFILE_SERVER_VERSION** or **PR_PROFILE_SERVER_FULL_VERSION** is likely to exist in a profile, but there is no guarantee that either always exists in a profile.</span></span> <span data-ttu-id="66e85-126">Outlook no se escribe en cualquiera de las propiedades hasta que se haya conectado correctamente al servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="66e85-126">Outlook does not write to either property until it has successfully connected to the Exchange Server.</span></span> 
  
<span data-ttu-id="66e85-127">En el modelo de objetos de Outlook, puede usar la propiedad **ExchangeMailboxServerVersion** del objeto **NameSpace** para buscar la versión de Exchange Server en el que se hospeda el buzón activo.</span><span class="sxs-lookup"><span data-stu-id="66e85-127">In the Outlook object model, you can use the **ExchangeMailboxServerVersion** property of the **NameSpace** object to find the version of Exchange Server on which the active mailbox is hosted.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="66e85-128">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="66e85-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="66e85-129">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="66e85-129">Protocol specifications</span></span>

<span data-ttu-id="66e85-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="66e85-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="66e85-131">Proporciona definiciones de conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="66e85-131">Provides property set definitions.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="66e85-132">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="66e85-132">Header files</span></span>

<span data-ttu-id="66e85-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="66e85-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="66e85-134">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="66e85-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="66e85-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="66e85-135">Mapitags.h</span></span>
  
> <span data-ttu-id="66e85-136">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="66e85-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="66e85-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="66e85-137">See also</span></span>



[<span data-ttu-id="66e85-138">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="66e85-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="66e85-139">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="66e85-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="66e85-140">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="66e85-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="66e85-141">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="66e85-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

