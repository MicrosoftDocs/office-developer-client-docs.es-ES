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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286569"
---
# <a name="pidtagprofileserverversion-canonical-property"></a><span data-ttu-id="3b8dd-103">Propiedad canónica PidTagProfileServerVersion</span><span class="sxs-lookup"><span data-stu-id="3b8dd-103">PidTagProfileServerVersion Canonical Property</span></span>

  
  
<span data-ttu-id="3b8dd-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3b8dd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3b8dd-105">Especifica información sobre la versión de Microsoft Exchange Server a la que están conectadas las cuentas de un perfil Outlook Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3b8dd-105">Specifies information about the version of Microsoft Exchange Server to which accounts in a Microsoft Outlook profile are connected.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="3b8dd-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="3b8dd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3b8dd-107">PR_PROFILE_SERVER_VERSION</span><span class="sxs-lookup"><span data-stu-id="3b8dd-107">PR_PROFILE_SERVER_VERSION</span></span>  <br/> |
|<span data-ttu-id="3b8dd-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="3b8dd-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3b8dd-109">0x661B</span><span class="sxs-lookup"><span data-stu-id="3b8dd-109">0x661B</span></span>  <br/> |
|<span data-ttu-id="3b8dd-110">Tipo de propiedad:</span><span class="sxs-lookup"><span data-stu-id="3b8dd-110">Property type:</span></span>  <br/> |<span data-ttu-id="3b8dd-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="3b8dd-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="3b8dd-112">Área:</span><span class="sxs-lookup"><span data-stu-id="3b8dd-112">Area:</span></span>  <br/> |<span data-ttu-id="3b8dd-113">Configuración de perfil MAPI</span><span class="sxs-lookup"><span data-stu-id="3b8dd-113">MAPI profile configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3b8dd-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3b8dd-114">Remarks</span></span>

<span data-ttu-id="3b8dd-115">Un perfil puede especificar una o varias cuentas que se conectan a un Exchange Server, pero deben estar conectadas al mismo Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="3b8dd-115">A profile can specify one or more accounts that connect to an Exchange Server, but they must be connected to the same Exchange Server.</span></span>
  
<span data-ttu-id="3b8dd-116">Las versiones Outlook anteriores Microsoft Office Outlook 2007 pueden escribir en esta propiedad para almacenar información sobre la versión de Exchange Server a la que está conectado el perfil activo.</span><span class="sxs-lookup"><span data-stu-id="3b8dd-116">Versions of Outlook earlier than Microsoft Office Outlook 2007 can write to this property to store information about the version of Exchange Server to which the active profile is connected.</span></span> <span data-ttu-id="3b8dd-117">Sin embargo, el formato de la información de versión varía para las diferentes versiones de Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="3b8dd-117">However, the format of the version information varies for different versions of Exchange Server.</span></span> <span data-ttu-id="3b8dd-118">Por ejemplo, Outlook almacena en **PR_PROFILE_SERVER_VERSION** el valor decimal 6944 para representar solo el número de compilación principal en el identificador de versión **de 6.5.6944.3** para Microsoft Exchange Server 2003.</span><span class="sxs-lookup"><span data-stu-id="3b8dd-118">For example, Outlook stores in **PR_PROFILE_SERVER_VERSION** the decimal value 6944 to represent only the major build number in the version identifier of **6.5.6944.3** for Microsoft Exchange Server 2003.</span></span> <span data-ttu-id="3b8dd-119">Para una conexión Exchange 2007, Outlook almacena el número de versión principal y el número de compilación principal en una representación hexadecimal concatenada de estos números en la propiedad.</span><span class="sxs-lookup"><span data-stu-id="3b8dd-119">For an Exchange 2007 connection, Outlook stores the major version number and the major build number in a concatenated hexadecimal representation of these numbers in the property.</span></span> <span data-ttu-id="3b8dd-120">Un Exchange de versión de 2007 de **8.0.685.24** tiene un número de versión principal 8 y un número de compilación principal 685 en decimal.</span><span class="sxs-lookup"><span data-stu-id="3b8dd-120">An Exchange 2007 version identifier of **8.0.685.24** has a major version number 8 and a major build number 685 in decimal.</span></span> <span data-ttu-id="3b8dd-121">Al convertir ambos números en hexadecimales, obtiene 0x8 y 0x2AD.</span><span class="sxs-lookup"><span data-stu-id="3b8dd-121">Converting both numbers to hexadecimal, you get 0x8 and 0x2AD.</span></span> <span data-ttu-id="3b8dd-122">Concatenando estos dos números, Outlook el valor 0x82AD en **PR_PROFILE_SERVER_VERSION** en representación hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="3b8dd-122">Concatenating these two numbers, Outlook stores the value 0x82AD in **PR_PROFILE_SERVER_VERSION** in hexadecimal representation.</span></span> 
  
<span data-ttu-id="3b8dd-123">Outlook 2007 no lee ni escribe en esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="3b8dd-123">Outlook 2007 does not read or write to this property.</span></span> <span data-ttu-id="3b8dd-124">Admite **[PR_PROFILE_SERVER_FULL_VERSION](pidtagprofileserverfullversion-canonical-property.md)**.</span><span class="sxs-lookup"><span data-stu-id="3b8dd-124">It supports **[PR_PROFILE_SERVER_FULL_VERSION](pidtagprofileserverfullversion-canonical-property.md)**.</span></span> 
  
<span data-ttu-id="3b8dd-125">Es probable **que PR_PROFILE_SERVER_VERSION** o **PR_PROFILE_SERVER_FULL_VERSION** un perfil, pero no existe ninguna garantía de que exista siempre en un perfil.</span><span class="sxs-lookup"><span data-stu-id="3b8dd-125">Only one of **PR_PROFILE_SERVER_VERSION** or **PR_PROFILE_SERVER_FULL_VERSION** is likely to exist in a profile, but there is no guarantee that either always exists in a profile.</span></span> <span data-ttu-id="3b8dd-126">Outlook no escribe en ninguna de las propiedades hasta que se haya conectado correctamente al Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="3b8dd-126">Outlook does not write to either property until it has successfully connected to the Exchange Server.</span></span> 
  
<span data-ttu-id="3b8dd-127">En el Outlook de objetos, puede usar la propiedad **ExchangeMailboxServerVersion** del objeto **NameSpace** para buscar la versión de Exchange Server en la que se hospeda el buzón activo.</span><span class="sxs-lookup"><span data-stu-id="3b8dd-127">In the Outlook object model, you can use the **ExchangeMailboxServerVersion** property of the **NameSpace** object to find the version of Exchange Server on which the active mailbox is hosted.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="3b8dd-128">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="3b8dd-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3b8dd-129">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="3b8dd-129">Protocol specifications</span></span>

<span data-ttu-id="3b8dd-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3b8dd-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3b8dd-131">Proporciona definiciones de conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="3b8dd-131">Provides property set definitions.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3b8dd-132">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="3b8dd-132">Header files</span></span>

<span data-ttu-id="3b8dd-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3b8dd-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="3b8dd-134">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="3b8dd-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="3b8dd-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3b8dd-135">Mapitags.h</span></span>
  
> <span data-ttu-id="3b8dd-136">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="3b8dd-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3b8dd-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="3b8dd-137">See also</span></span>



[<span data-ttu-id="3b8dd-138">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="3b8dd-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3b8dd-139">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="3b8dd-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3b8dd-140">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="3b8dd-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3b8dd-141">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="3b8dd-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

