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
# <a name="pidtagprofileserverversion-canonical-property"></a><span data-ttu-id="0499c-103">Propiedad canónica PidTagProfileServerVersion</span><span class="sxs-lookup"><span data-stu-id="0499c-103">PidTagProfileServerVersion Canonical Property</span></span>

  
  
<span data-ttu-id="0499c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0499c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0499c-105">Especifica información sobre la versión de Microsoft Exchange Server a la que se conectan las cuentas de un perfil de Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="0499c-105">Specifies information about the version of Microsoft Exchange Server to which accounts in a Microsoft Outlook profile are connected.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="0499c-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="0499c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0499c-107">PR_PROFILE_SERVER_VERSION</span><span class="sxs-lookup"><span data-stu-id="0499c-107">PR_PROFILE_SERVER_VERSION</span></span>  <br/> |
|<span data-ttu-id="0499c-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="0499c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0499c-109">0x661B</span><span class="sxs-lookup"><span data-stu-id="0499c-109">0x661B</span></span>  <br/> |
|<span data-ttu-id="0499c-110">Tipo de propiedad:</span><span class="sxs-lookup"><span data-stu-id="0499c-110">Property type:</span></span>  <br/> |<span data-ttu-id="0499c-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="0499c-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="0499c-112">Área:</span><span class="sxs-lookup"><span data-stu-id="0499c-112">Area:</span></span>  <br/> |<span data-ttu-id="0499c-113">Configuración del perfil MAPI</span><span class="sxs-lookup"><span data-stu-id="0499c-113">MAPI profile configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0499c-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0499c-114">Remarks</span></span>

<span data-ttu-id="0499c-115">Un perfil puede especificar una o más cuentas que se conectan a un servidor de Exchange, pero deben estar conectadas al mismo servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="0499c-115">A profile can specify one or more accounts that connect to an Exchange Server, but they must be connected to the same Exchange Server.</span></span>
  
<span data-ttu-id="0499c-116">Las versiones de Outlook anteriores a Microsoft Office Outlook 2007 pueden escribir en esta propiedad para almacenar información acerca de la versión de Exchange Server a la que está conectado el perfil activo.</span><span class="sxs-lookup"><span data-stu-id="0499c-116">Versions of Outlook earlier than Microsoft Office Outlook 2007 can write to this property to store information about the version of Exchange Server to which the active profile is connected.</span></span> <span data-ttu-id="0499c-117">Sin embargo, el formato de la información de versión varía para las diferentes versiones de Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="0499c-117">However, the format of the version information varies for different versions of Exchange Server.</span></span> <span data-ttu-id="0499c-118">Por ejemplo, Outlook almacena en **PR_PROFILE_SERVER_VERSION** el valor decimal 6944 para representar solo el número de compilación principal en el identificador de la versión de **6.5.6944.3** para Microsoft Exchange Server 2003.</span><span class="sxs-lookup"><span data-stu-id="0499c-118">For example, Outlook stores in **PR_PROFILE_SERVER_VERSION** the decimal value 6944 to represent only the major build number in the version identifier of **6.5.6944.3** for Microsoft Exchange Server 2003.</span></span> <span data-ttu-id="0499c-119">Para una conexión de Exchange 2007, Outlook almacena el número de versión principal y el número de compilación principal en una representación hexadecimal concatenada de estos números en la propiedad.</span><span class="sxs-lookup"><span data-stu-id="0499c-119">For an Exchange 2007 connection, Outlook stores the major version number and the major build number in a concatenated hexadecimal representation of these numbers in the property.</span></span> <span data-ttu-id="0499c-120">Un identificador de versión de Exchange 2007 de **8.0.685.24** tiene un número de versión 8 principal y un número de compilación superior 685 en decimal.</span><span class="sxs-lookup"><span data-stu-id="0499c-120">An Exchange 2007 version identifier of **8.0.685.24** has a major version number 8 and a major build number 685 in decimal.</span></span> <span data-ttu-id="0499c-121">Al convertir ambos números a hexadecimal, se obtiene 0x8 y 0x2AD.</span><span class="sxs-lookup"><span data-stu-id="0499c-121">Converting both numbers to hexadecimal, you get 0x8 and 0x2AD.</span></span> <span data-ttu-id="0499c-122">Concatenación de estos dos números, Outlook almacena el valor 0x82AD en **PR_PROFILE_SERVER_VERSION** en representación hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="0499c-122">Concatenating these two numbers, Outlook stores the value 0x82AD in **PR_PROFILE_SERVER_VERSION** in hexadecimal representation.</span></span> 
  
<span data-ttu-id="0499c-123">Outlook 2007 no lee ni escribe en esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="0499c-123">Outlook 2007 does not read or write to this property.</span></span> <span data-ttu-id="0499c-124">Admite **[PR_PROFILE_SERVER_FULL_VERSION](pidtagprofileserverfullversion-canonical-property.md)**.</span><span class="sxs-lookup"><span data-stu-id="0499c-124">It supports **[PR_PROFILE_SERVER_FULL_VERSION](pidtagprofileserverfullversion-canonical-property.md)**.</span></span> 
  
<span data-ttu-id="0499c-125">Es probable que solo exista un **PR_PROFILE_SERVER_VERSION** o **PR_PROFILE_SERVER_FULL_VERSION** en un perfil, pero no hay ninguna garantía que siempre exista en un perfil.</span><span class="sxs-lookup"><span data-stu-id="0499c-125">Only one of **PR_PROFILE_SERVER_VERSION** or **PR_PROFILE_SERVER_FULL_VERSION** is likely to exist in a profile, but there is no guarantee that either always exists in a profile.</span></span> <span data-ttu-id="0499c-126">Outlook no escribe en ninguna de las dos propiedades hasta que se haya conectado correctamente al servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="0499c-126">Outlook does not write to either property until it has successfully connected to the Exchange Server.</span></span> 
  
<span data-ttu-id="0499c-127">En el modelo de objetos de Outlook, puede usar la propiedad **ExchangeMailboxServerVersion** del objeto **namespace** para buscar la versión de Exchange Server en la que se hospeda el buzón activo.</span><span class="sxs-lookup"><span data-stu-id="0499c-127">In the Outlook object model, you can use the **ExchangeMailboxServerVersion** property of the **NameSpace** object to find the version of Exchange Server on which the active mailbox is hosted.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="0499c-128">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="0499c-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0499c-129">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="0499c-129">Protocol specifications</span></span>

<span data-ttu-id="0499c-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0499c-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0499c-131">Proporciona definiciones de conjuntos de propiedades.</span><span class="sxs-lookup"><span data-stu-id="0499c-131">Provides property set definitions.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0499c-132">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="0499c-132">Header files</span></span>

<span data-ttu-id="0499c-133">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="0499c-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="0499c-134">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="0499c-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="0499c-135">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="0499c-135">Mapitags.h</span></span>
  
> <span data-ttu-id="0499c-136">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="0499c-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0499c-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="0499c-137">See also</span></span>



[<span data-ttu-id="0499c-138">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="0499c-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0499c-139">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="0499c-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0499c-140">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="0499c-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0499c-141">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="0499c-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

