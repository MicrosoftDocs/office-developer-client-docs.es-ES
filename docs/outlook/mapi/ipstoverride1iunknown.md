---
title: IPSTOVERRIDE1 IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTOVERRIDE1
api_type:
- COM
ms.assetid: d26cee81-45ea-4fd3-8a54-5f35264b5d6a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 5208e77f3605b5ba861f68786d8fe5e91b990d32
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315501"
---
# <a name="ipstoverride1--iunknown"></a><span data-ttu-id="c06d9-103">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c06d9-103">IPSTOVERRIDE1 : IUnknown</span></span>

  
  
<span data-ttu-id="c06d9-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c06d9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c06d9-105">Permite que un proveedor de almacenamiento de archivos de carpetas personales (PST) invalide la directiva PSTDisableGrow.</span><span class="sxs-lookup"><span data-stu-id="c06d9-105">Allows a Personal Folders file (PST) store provider to override the PSTDisableGrow policy.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c06d9-106">Hereda de:</span><span class="sxs-lookup"><span data-stu-id="c06d9-106">Inherits from:</span></span>  <br/> |<span data-ttu-id="c06d9-107">IUnknown</span><span class="sxs-lookup"><span data-stu-id="c06d9-107">IUnknown</span></span>  <br/> |
|<span data-ttu-id="c06d9-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="c06d9-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c06d9-109">Proveedor de almacenamiento PST</span><span class="sxs-lookup"><span data-stu-id="c06d9-109">PST store provider</span></span>  <br/> |
|<span data-ttu-id="c06d9-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="c06d9-110">Called by:</span></span>  <br/> |<span data-ttu-id="c06d9-111">Cliente</span><span class="sxs-lookup"><span data-stu-id="c06d9-111">Client</span></span>  <br/> |
|<span data-ttu-id="c06d9-112">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="c06d9-112">Interface identifier:</span></span>  <br/> |<span data-ttu-id="c06d9-113">IID_IPSTOVERRIDE1</span><span class="sxs-lookup"><span data-stu-id="c06d9-113">IID_IPSTOVERRIDE1</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="c06d9-114">Orden de Vtable</span><span class="sxs-lookup"><span data-stu-id="c06d9-114">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="c06d9-115">IPSTOVERRIDE1::GetPersistedRegistrations</span><span class="sxs-lookup"><span data-stu-id="c06d9-115">IPSTOVERRIDE1::GetPersistedRegistrations</span></span>](ipstoverride1-getpersistedregistrations.md) <br/> |<span data-ttu-id="c06d9-116">Recupera la lista de registros del archivo Carpetas personales (.pst).</span><span class="sxs-lookup"><span data-stu-id="c06d9-116">Retrieves the list of registrations for the Personal Folders (.pst) file.</span></span>  <br/> |
|[<span data-ttu-id="c06d9-117">IPSTOVERRIDE1::SetPersistedRegistrations</span><span class="sxs-lookup"><span data-stu-id="c06d9-117">IPSTOVERRIDE1::SetPersistedRegistrations</span></span>](ipstoverride1-setpersistedregistrations.md) <br/> |<span data-ttu-id="c06d9-118">Registra archivos de carpetas personales para el desbloqueo automático, evitando más llamadas a HrTrustedPSTOverrideHandlerCallback.</span><span class="sxs-lookup"><span data-stu-id="c06d9-118">Registers Personal Folders files for automatic unlocking, avoiding further calls to HrTrustedPSTOverrideHandlerCallback.</span></span>  <br/> |
|[<span data-ttu-id="c06d9-119">IPSTOVERRIDE1::OverridePSTDisableGrow</span><span class="sxs-lookup"><span data-stu-id="c06d9-119">IPSTOVERRIDE1::OverridePSTDisableGrow</span></span>](ipstoverride1-overridepstdisablegrow.md) <br/> |<span data-ttu-id="c06d9-120">Desbloquea un archivo de carpetas personales para su crecimiento.</span><span class="sxs-lookup"><span data-stu-id="c06d9-120">Unlocks a Personal Folders file for growth.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c06d9-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c06d9-121">Remarks</span></span>

<span data-ttu-id="c06d9-122">Es posible que los identificadores de interfaz de controlador de invalidación de PST no se definan en el archivo de encabezado descargable que tiene actualmente, en cuyo caso los encontrará en el tema Constantes [MAPI](mapi-constants.md) y puede copiarlos y agregarlos al código.</span><span class="sxs-lookup"><span data-stu-id="c06d9-122">The PST Override Handler Interface Identifiers might not be defined in the downloadable header file you currently have, in which case you will find them in the [MAPI Constants](mapi-constants.md) topic, and can copy and add them to your code.</span></span> <span data-ttu-id="c06d9-123">Use la macro DEFINE_GUID definida en el archivo de encabezado guiddef.h del Kit de desarrollo de software (SDK) de Microsoft Windows para asociar nombres simbólicos de identificador único global (GUID) con sus valores.</span><span class="sxs-lookup"><span data-stu-id="c06d9-123">Use the DEFINE_GUID macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate globally unique identifier (GUID) symbolic names with their values.</span></span> 
  
<span data-ttu-id="c06d9-124">Para obtener más información, vea [How to implement a PST override handler to bypass the PSTDisableGrow policy in Outlook 2007](https://support.microsoft.com/kb/956070).</span><span class="sxs-lookup"><span data-stu-id="c06d9-124">For more information see [How to implement a PST override handler to bypass the PSTDisableGrow policy in Outlook 2007](https://support.microsoft.com/kb/956070).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c06d9-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="c06d9-125">See also</span></span>



[<span data-ttu-id="c06d9-126">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c06d9-126">IPSTOVERRIDEREQ : IUnknown</span></span>](ipstoverridereqiunknown.md)

