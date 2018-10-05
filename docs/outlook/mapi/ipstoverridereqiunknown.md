---
title: IPSTOVERRIDEREQ IUnknown
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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389109"
---
# <a name="ipstoverridereq--iunknown"></a><span data-ttu-id="990f6-103">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="990f6-103">IPSTOVERRIDEREQ : IUnknown</span></span>

  
  
<span data-ttu-id="990f6-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="990f6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="990f6-105">Proveedor de almacén de recursos de acceso de un archivo de carpetas personales (PST).</span><span class="sxs-lookup"><span data-stu-id="990f6-105">Accesses resources of a Personal Folders file (PST) store provider.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="990f6-106">Hereda de:</span><span class="sxs-lookup"><span data-stu-id="990f6-106">Inherits from:</span></span>  <br/> |<span data-ttu-id="990f6-107">IUnknown</span><span class="sxs-lookup"><span data-stu-id="990f6-107">IUnknown</span></span>  <br/> |
|<span data-ttu-id="990f6-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="990f6-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="990f6-109">Proveedor de almacén de archivos PST</span><span class="sxs-lookup"><span data-stu-id="990f6-109">PST store provider</span></span>  <br/> |
|<span data-ttu-id="990f6-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="990f6-110">Called by:</span></span>  <br/> |<span data-ttu-id="990f6-111">Aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="990f6-111">Client applications</span></span>  <br/> |
|<span data-ttu-id="990f6-112">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="990f6-112">Interface identifier:</span></span>  <br/> |<span data-ttu-id="990f6-113">IID_IPSTOVERRIDEREQ</span><span class="sxs-lookup"><span data-stu-id="990f6-113">IID_IPSTOVERRIDEREQ</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="990f6-114">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="990f6-114">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="990f6-115">IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler</span><span class="sxs-lookup"><span data-stu-id="990f6-115">IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler</span></span>](ipstoverridereq-registertrustedpstoverridehandler.md) <br/> |<span data-ttu-id="990f6-116">Inicia el procedimiento de desbloqueo para un archivo de carpetas personales (.pst).</span><span class="sxs-lookup"><span data-stu-id="990f6-116">Initiates the unlocking procedure for a Personal Folders (.pst) file.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="990f6-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="990f6-117">Remarks</span></span>

<span data-ttu-id="990f6-118">Los identificadores de interfaz de controlador de invalidar PST no puede definirse en el archivo de encabezado que se pueden descargar que tiene actualmente, en cuyo caso se encontrarlos en el tema de [Las constantes de MAPI](mapi-constants.md) y puede copiar y agregarlos a su código.</span><span class="sxs-lookup"><span data-stu-id="990f6-118">The PST Override Handler Interface Identifiers might not be defined in the downloadable header file you currently have, in which case you will find them in the [MAPI Constants](mapi-constants.md) topic, and can copy and add them to your code.</span></span> <span data-ttu-id="990f6-119">Use la macro DEFINE_GUID definida en el guiddef.h de archivo de encabezado de Kit de desarrollo de Software (SDK) de Microsoft Windows para asociar los nombres simbólicos de identificador único global (GUID) con sus valores.</span><span class="sxs-lookup"><span data-stu-id="990f6-119">Use the DEFINE_GUID macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate globally unique identifier (GUID) symbolic names with their values.</span></span> 
  
<span data-ttu-id="990f6-120">Para obtener más información, vea [cómo implementar un controlador de reemplazo de PST para que omita la directiva de PSTDisableGrow en Outlook 2007](https://support.microsoft.com/kb/956070).</span><span class="sxs-lookup"><span data-stu-id="990f6-120">For more information see [How to implement a PST override handler to bypass the PSTDisableGrow policy in Outlook 2007](https://support.microsoft.com/kb/956070).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="990f6-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="990f6-121">See also</span></span>



[<span data-ttu-id="990f6-122">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="990f6-122">IPSTOVERRIDE1 : IUnknown</span></span>](ipstoverride1iunknown.md)

