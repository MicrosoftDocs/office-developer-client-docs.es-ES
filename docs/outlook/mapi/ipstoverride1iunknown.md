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
ms.openlocfilehash: db2853080b1fc2ff3a346dcfb8d112237b7f3459
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817944"
---
# <a name="ipstoverride1--iunknown"></a><span data-ttu-id="254c0-103">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="254c0-103">IPSTOVERRIDE1 : IUnknown</span></span>

  
  
<span data-ttu-id="254c0-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="254c0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="254c0-105">Permite a un proveedor de almacén de carpetas personales (PST) de archivo invalidar la directiva PSTDisableGrow.</span><span class="sxs-lookup"><span data-stu-id="254c0-105">Allows a Personal Folders file (PST) store provider to override the PSTDisableGrow policy.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="254c0-106">Hereda de:</span><span class="sxs-lookup"><span data-stu-id="254c0-106">Inherits from:</span></span>  <br/> |<span data-ttu-id="254c0-107">IUnknown</span><span class="sxs-lookup"><span data-stu-id="254c0-107">IUnknown</span></span>  <br/> |
|<span data-ttu-id="254c0-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="254c0-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="254c0-109">Proveedor de almacén de archivos PST</span><span class="sxs-lookup"><span data-stu-id="254c0-109">PST store provider</span></span>  <br/> |
|<span data-ttu-id="254c0-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="254c0-110">Called by:</span></span>  <br/> |<span data-ttu-id="254c0-111">Cliente</span><span class="sxs-lookup"><span data-stu-id="254c0-111">Client</span></span>  <br/> |
|<span data-ttu-id="254c0-112">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="254c0-112">Interface identifier:</span></span>  <br/> |<span data-ttu-id="254c0-113">IID_IPSTOVERRIDE1</span><span class="sxs-lookup"><span data-stu-id="254c0-113">IID_IPSTOVERRIDE1</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="254c0-114">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="254c0-114">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="254c0-115">IPSTOVERRIDE1::GetPersistedRegistrations</span><span class="sxs-lookup"><span data-stu-id="254c0-115">IPSTOVERRIDE1::GetPersistedRegistrations</span></span>](ipstoverride1-getpersistedregistrations.md) <br/> |<span data-ttu-id="254c0-116">Recupera la lista de registros para el archivo de carpetas personales (.pst).</span><span class="sxs-lookup"><span data-stu-id="254c0-116">Retrieves the list of registrations for the Personal Folders (.pst) file.</span></span>  <br/> |
|[<span data-ttu-id="254c0-117">IPSTOVERRIDE1::SetPersistedRegistrations</span><span class="sxs-lookup"><span data-stu-id="254c0-117">IPSTOVERRIDE1::SetPersistedRegistrations</span></span>](ipstoverride1-setpersistedregistrations.md) <br/> |<span data-ttu-id="254c0-118">Registra los archivos de carpetas personales para el desbloqueo automático, evitar más llamadas a HrTrustedPSTOverrideHandlerCallback.</span><span class="sxs-lookup"><span data-stu-id="254c0-118">Registers Personal Folders files for automatic unlocking, avoiding further calls to HrTrustedPSTOverrideHandlerCallback.</span></span>  <br/> |
|[<span data-ttu-id="254c0-119">IPSTOVERRIDE1::OverridePSTDisableGrow</span><span class="sxs-lookup"><span data-stu-id="254c0-119">IPSTOVERRIDE1::OverridePSTDisableGrow</span></span>](ipstoverride1-overridepstdisablegrow.md) <br/> |<span data-ttu-id="254c0-120">Desbloquea un archivo de carpetas personales para el crecimiento.</span><span class="sxs-lookup"><span data-stu-id="254c0-120">Unlocks a Personal Folders file for growth.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="254c0-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="254c0-121">Remarks</span></span>

<span data-ttu-id="254c0-122">Los identificadores de interfaz de controlador de invalidar PST no puede definirse en el archivo de encabezado que se pueden descargar que tiene actualmente, en cuyo caso se encontrarlos en el tema de [Las constantes de MAPI](mapi-constants.md) y puede copiar y agregarlos a su código.</span><span class="sxs-lookup"><span data-stu-id="254c0-122">The PST Override Handler Interface Identifiers might not be defined in the downloadable header file you currently have, in which case you will find them in the [MAPI Constants](mapi-constants.md) topic, and can copy and add them to your code.</span></span> <span data-ttu-id="254c0-123">Use la macro DEFINE_GUID definida en el guiddef.h de archivo de encabezado de Kit de desarrollo de Software (SDK) de Microsoft Windows para asociar los nombres simbólicos de identificador único global (GUID) con sus valores.</span><span class="sxs-lookup"><span data-stu-id="254c0-123">Use the DEFINE_GUID macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate globally unique identifier (GUID) symbolic names with their values.</span></span> 
  
<span data-ttu-id="254c0-124">Para obtener más información, vea [cómo implementar un controlador de reemplazo de PST para que omita la directiva de PSTDisableGrow en Outlook 2007](http://support.microsoft.com/kb/956070).</span><span class="sxs-lookup"><span data-stu-id="254c0-124">For more information see [How to implement a PST override handler to bypass the PSTDisableGrow policy in Outlook 2007](http://support.microsoft.com/kb/956070).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="254c0-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="254c0-125">See also</span></span>



[<span data-ttu-id="254c0-126">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="254c0-126">IPSTOVERRIDEREQ : IUnknown</span></span>](ipstoverridereqiunknown.md)

