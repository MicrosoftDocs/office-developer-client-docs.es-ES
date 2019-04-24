---
title: IUnknown IPSTOVERRIDEREQ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTOVERRIDEREQ
api_type:
- COM
ms.assetid: 22f497de-4afe-4433-965d-c3b5a66b05da
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7f3f6ae2b9849710bf44d3635fc7bb9a62016f48
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356983"
---
# <a name="ipstoverridereq--iunknown"></a><span data-ttu-id="7f1a9-103">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7f1a9-103">IPSTOVERRIDEREQ : IUnknown</span></span>

  
  
<span data-ttu-id="7f1a9-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7f1a9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7f1a9-105">Tiene acceso a los recursos de un proveedor de almacenamiento de archivos de carpetas personales (PST).</span><span class="sxs-lookup"><span data-stu-id="7f1a9-105">Accesses resources of a Personal Folders file (PST) store provider.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7f1a9-106">Hereda de:</span><span class="sxs-lookup"><span data-stu-id="7f1a9-106">Inherits from:</span></span>  <br/> |<span data-ttu-id="7f1a9-107">IUnknown</span><span class="sxs-lookup"><span data-stu-id="7f1a9-107">IUnknown</span></span>  <br/> |
|<span data-ttu-id="7f1a9-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="7f1a9-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="7f1a9-109">Proveedor de almacén PST</span><span class="sxs-lookup"><span data-stu-id="7f1a9-109">PST store provider</span></span>  <br/> |
|<span data-ttu-id="7f1a9-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="7f1a9-110">Called by:</span></span>  <br/> |<span data-ttu-id="7f1a9-111">Aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="7f1a9-111">Client applications</span></span>  <br/> |
|<span data-ttu-id="7f1a9-112">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="7f1a9-112">Interface identifier:</span></span>  <br/> |<span data-ttu-id="7f1a9-113">IID_IPSTOVERRIDEREQ</span><span class="sxs-lookup"><span data-stu-id="7f1a9-113">IID_IPSTOVERRIDEREQ</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="7f1a9-114">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="7f1a9-114">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="7f1a9-115">IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler</span><span class="sxs-lookup"><span data-stu-id="7f1a9-115">IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler</span></span>](ipstoverridereq-registertrustedpstoverridehandler.md) <br/> |<span data-ttu-id="7f1a9-116">Inicia el proceso de desbloqueo de un archivo de carpetas personales (. pst).</span><span class="sxs-lookup"><span data-stu-id="7f1a9-116">Initiates the unlocking procedure for a Personal Folders (.pst) file.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7f1a9-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7f1a9-117">Remarks</span></span>

<span data-ttu-id="7f1a9-118">Es posible que los identificadores de interfaz del controlador de anulación de PST no estén definidos en el archivo de encabezado descargable que tiene actualmente, en cuyo caso los encontrará en el tema sobre [constantes MAPI](mapi-constants.md) y puede copiarlos y agregarlos al código.</span><span class="sxs-lookup"><span data-stu-id="7f1a9-118">The PST Override Handler Interface Identifiers might not be defined in the downloadable header file you currently have, in which case you will find them in the [MAPI Constants](mapi-constants.md) topic, and can copy and add them to your code.</span></span> <span data-ttu-id="7f1a9-119">Use la macro DEFINE_GUID definida en el archivo de encabezado guiddef. h del kit de desarrollo de software (SDK) de Microsoft Windows para asociar nombres simbólicos de identificador único global (GUID) con sus valores.</span><span class="sxs-lookup"><span data-stu-id="7f1a9-119">Use the DEFINE_GUID macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate globally unique identifier (GUID) symbolic names with their values.</span></span> 
  
<span data-ttu-id="7f1a9-120">Para obtener más información, vea [cómo implementar un controlador de reemplazo de PST para omitir la Directiva PSTDisableGrow en Outlook 2007](https://support.microsoft.com/kb/956070).</span><span class="sxs-lookup"><span data-stu-id="7f1a9-120">For more information see [How to implement a PST override handler to bypass the PSTDisableGrow policy in Outlook 2007](https://support.microsoft.com/kb/956070).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7f1a9-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="7f1a9-121">See also</span></span>



[<span data-ttu-id="7f1a9-122">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7f1a9-122">IPSTOVERRIDE1 : IUnknown</span></span>](ipstoverride1iunknown.md)

