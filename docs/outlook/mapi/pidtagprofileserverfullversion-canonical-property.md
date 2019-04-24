---
title: Propiedad canónica PidTagProfileServerFullVersion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8c88a625-da57-3b1d-9887-0a898b722766
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 9456178e9426d7a5fe17382d876f507daa0251f4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341604"
---
# <a name="pidtagprofileserverfullversion-canonical-property"></a><span data-ttu-id="4c587-103">Propiedad canónica PidTagProfileServerFullVersion</span><span class="sxs-lookup"><span data-stu-id="4c587-103">PidTagProfileServerFullVersion Canonical Property</span></span>

  
  
<span data-ttu-id="4c587-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4c587-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4c587-105">Especifica la versión completa y la información de compilación sobre el servidor de Microsoft Exchange al que se conectan las cuentas de un perfil.</span><span class="sxs-lookup"><span data-stu-id="4c587-105">Specifies complete version and build information about the Microsoft Exchange Server to which accounts in a profile are connected.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="4c587-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="4c587-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4c587-107">PR_PROFILE_SERVER_FULL_VERSION</span><span class="sxs-lookup"><span data-stu-id="4c587-107">PR_PROFILE_SERVER_FULL_VERSION</span></span>  <br/> |
|<span data-ttu-id="4c587-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="4c587-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4c587-109">0x663B</span><span class="sxs-lookup"><span data-stu-id="4c587-109">0x663B</span></span>  <br/> |
|<span data-ttu-id="4c587-110">Tipo de propiedad:</span><span class="sxs-lookup"><span data-stu-id="4c587-110">Property type:</span></span>  <br/> |<span data-ttu-id="4c587-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="4c587-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="4c587-112">Área:</span><span class="sxs-lookup"><span data-stu-id="4c587-112">Area:</span></span>  <br/> |<span data-ttu-id="4c587-113">Configuración del perfil MAPI</span><span class="sxs-lookup"><span data-stu-id="4c587-113">MAPI profile configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4c587-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4c587-114">Remarks</span></span>

<span data-ttu-id="4c587-115">Un perfil puede especificar una o más cuentas que se conectan a un servidor de Exchange, pero deben estar conectadas al mismo servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="4c587-115">A profile can specify one or more accounts that connect to an Exchange Server, but they must be connected to the same Exchange Server.</span></span>
  
<span data-ttu-id="4c587-116">Las versiones de Outlook anteriores a Microsoft Office Outlook 2007 no admiten esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="4c587-116">Versions of Outlook earlier than Microsoft Office Outlook 2007 do not support this property.</span></span> <span data-ttu-id="4c587-117">Para esas versiones de Outlook, Compruebe la existencia de **[PR_PROFILE_SERVER_VERSION](pidtagprofileserverversion-canonical-property.md)** en el perfil.</span><span class="sxs-lookup"><span data-stu-id="4c587-117">For those versions of Outlook, check for the existence of **[PR_PROFILE_SERVER_VERSION](pidtagprofileserverversion-canonical-property.md)** in the profile.</span></span> 
  
<span data-ttu-id="4c587-118">Por lo general, si el buzón activo está conectado a un servidor de Exchange, Outlook 2007 almacena información de la versión completa de Exchange Server en la propiedad **PR_PROFILE_SERVER_FULL_VERSION** del perfil activo.</span><span class="sxs-lookup"><span data-stu-id="4c587-118">Generally, if the active mailbox is connected to an Exchange Server, Outlook 2007 stores complete Exchange Server version information in the **PR_PROFILE_SERVER_FULL_VERSION** property in the active profile.</span></span> <span data-ttu-id="4c587-119">Outlook almacena la información en una estructura **EXCHANGE_STORE_VERSION_NUM** que contiene los números de versión principales y secundarias, así como los números de compilación principales y secundarias.</span><span class="sxs-lookup"><span data-stu-id="4c587-119">Outlook stores the information in an **EXCHANGE_STORE_VERSION_NUM** structure that contains the major and minor version numbers and the major and minor build numbers.</span></span> <span data-ttu-id="4c587-120">Por ejemplo, para almacenar el identificador de versión de Exchange Server de **8.0.685.24**, el número de versión principal es 8 y el número de versión secundaria es 0, y el número de compilación principal es 685 y el número de compilación menor es 24.</span><span class="sxs-lookup"><span data-stu-id="4c587-120">For example, to store the Exchange Server version identifier of **8.0.685.24**, the major version number is 8 and minor version number is 0, and the major build number is 685 and minor build number is 24.</span></span>
  
<span data-ttu-id="4c587-121">Es probable que solo exista un **PR_PROFILE_SERVER_VERSION** o **PR_PROFILE_SERVER_FULL_VERSION** en un perfil, pero no hay ninguna garantía que siempre exista en un perfil.</span><span class="sxs-lookup"><span data-stu-id="4c587-121">Only one of **PR_PROFILE_SERVER_VERSION** or **PR_PROFILE_SERVER_FULL_VERSION** is likely to exist in a profile, but there is no guarantee that either always exists in a profile.</span></span> <span data-ttu-id="4c587-122">Outlook no escribe en ninguna de las dos propiedades hasta que se haya conectado correctamente al servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="4c587-122">Outlook does not write to either property until it has successfully connected to the Exchange Server.</span></span> 
  
<span data-ttu-id="4c587-123">En el modelo de objetos de Outlook, puede usar la propiedad **ExchangeMailboxServerVersion** del objeto **namespace** para buscar la versión de Exchange Server en la que se hospeda el buzón activo.</span><span class="sxs-lookup"><span data-stu-id="4c587-123">In the Outlook object model, you can use the **ExchangeMailboxServerVersion** property of the **NameSpace** object to find the version of Exchange Server on which the active mailbox is hosted.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="4c587-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="4c587-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4c587-125">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="4c587-125">Protocol specifications</span></span>

<span data-ttu-id="4c587-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4c587-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4c587-127">Proporciona definiciones de conjuntos de propiedades.</span><span class="sxs-lookup"><span data-stu-id="4c587-127">Provides property set definitions.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4c587-128">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="4c587-128">Header files</span></span>

<span data-ttu-id="4c587-129">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="4c587-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="4c587-130">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="4c587-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="4c587-131">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="4c587-131">Mapitags.h</span></span>
  
> <span data-ttu-id="4c587-132">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="4c587-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4c587-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="4c587-133">See also</span></span>



[<span data-ttu-id="4c587-134">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="4c587-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4c587-135">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="4c587-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4c587-136">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="4c587-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4c587-137">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="4c587-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

