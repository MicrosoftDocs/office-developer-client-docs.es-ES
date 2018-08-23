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
ms.openlocfilehash: e73115811fe0009769826e0f6a011c489772f770
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569851"
---
# <a name="ipstoverride1--iunknown"></a><span data-ttu-id="cfeca-103">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cfeca-103">IPSTOVERRIDE1 : IUnknown</span></span>

  
  
<span data-ttu-id="cfeca-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cfeca-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cfeca-105">Permite a un proveedor de almacén de carpetas personales (PST) de archivo invalidar la directiva PSTDisableGrow.</span><span class="sxs-lookup"><span data-stu-id="cfeca-105">Allows a Personal Folders file (PST) store provider to override the PSTDisableGrow policy.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cfeca-106">Hereda de:</span><span class="sxs-lookup"><span data-stu-id="cfeca-106">Inherits from:</span></span>  <br/> |<span data-ttu-id="cfeca-107">IUnknown</span><span class="sxs-lookup"><span data-stu-id="cfeca-107">IUnknown</span></span>  <br/> |
|<span data-ttu-id="cfeca-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="cfeca-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="cfeca-109">Proveedor de almacén de archivos PST</span><span class="sxs-lookup"><span data-stu-id="cfeca-109">PST store provider</span></span>  <br/> |
|<span data-ttu-id="cfeca-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="cfeca-110">Called by:</span></span>  <br/> |<span data-ttu-id="cfeca-111">Cliente</span><span class="sxs-lookup"><span data-stu-id="cfeca-111">Client</span></span>  <br/> |
|<span data-ttu-id="cfeca-112">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="cfeca-112">Interface identifier:</span></span>  <br/> |<span data-ttu-id="cfeca-113">IID_IPSTOVERRIDE1</span><span class="sxs-lookup"><span data-stu-id="cfeca-113">IID_IPSTOVERRIDE1</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="cfeca-114">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="cfeca-114">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="cfeca-115">IPSTOVERRIDE1::GetPersistedRegistrations</span><span class="sxs-lookup"><span data-stu-id="cfeca-115">IPSTOVERRIDE1::GetPersistedRegistrations</span></span>](ipstoverride1-getpersistedregistrations.md) <br/> |<span data-ttu-id="cfeca-116">Recupera la lista de registros para el archivo de carpetas personales (.pst).</span><span class="sxs-lookup"><span data-stu-id="cfeca-116">Retrieves the list of registrations for the Personal Folders (.pst) file.</span></span>  <br/> |
|[<span data-ttu-id="cfeca-117">IPSTOVERRIDE1::SetPersistedRegistrations</span><span class="sxs-lookup"><span data-stu-id="cfeca-117">IPSTOVERRIDE1::SetPersistedRegistrations</span></span>](ipstoverride1-setpersistedregistrations.md) <br/> |<span data-ttu-id="cfeca-118">Registra los archivos de carpetas personales para el desbloqueo automático, evitar más llamadas a HrTrustedPSTOverrideHandlerCallback.</span><span class="sxs-lookup"><span data-stu-id="cfeca-118">Registers Personal Folders files for automatic unlocking, avoiding further calls to HrTrustedPSTOverrideHandlerCallback.</span></span>  <br/> |
|[<span data-ttu-id="cfeca-119">IPSTOVERRIDE1::OverridePSTDisableGrow</span><span class="sxs-lookup"><span data-stu-id="cfeca-119">IPSTOVERRIDE1::OverridePSTDisableGrow</span></span>](ipstoverride1-overridepstdisablegrow.md) <br/> |<span data-ttu-id="cfeca-120">Desbloquea un archivo de carpetas personales para el crecimiento.</span><span class="sxs-lookup"><span data-stu-id="cfeca-120">Unlocks a Personal Folders file for growth.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cfeca-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cfeca-121">Remarks</span></span>

<span data-ttu-id="cfeca-122">Los identificadores de interfaz de controlador de invalidar PST no puede definirse en el archivo de encabezado que se pueden descargar que tiene actualmente, en cuyo caso se encontrarlos en el tema de [Las constantes de MAPI](mapi-constants.md) y puede copiar y agregarlos a su código.</span><span class="sxs-lookup"><span data-stu-id="cfeca-122">The PST Override Handler Interface Identifiers might not be defined in the downloadable header file you currently have, in which case you will find them in the [MAPI Constants](mapi-constants.md) topic, and can copy and add them to your code.</span></span> <span data-ttu-id="cfeca-123">Use la macro DEFINE_GUID definida en el guiddef.h de archivo de encabezado de Kit de desarrollo de Software (SDK) de Microsoft Windows para asociar los nombres simbólicos de identificador único global (GUID) con sus valores.</span><span class="sxs-lookup"><span data-stu-id="cfeca-123">Use the DEFINE_GUID macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate globally unique identifier (GUID) symbolic names with their values.</span></span> 
  
<span data-ttu-id="cfeca-124">Para obtener más información, vea [cómo implementar un controlador de reemplazo de PST para que omita la directiva de PSTDisableGrow en Outlook 2007](http://support.microsoft.com/kb/956070).</span><span class="sxs-lookup"><span data-stu-id="cfeca-124">For more information see [How to implement a PST override handler to bypass the PSTDisableGrow policy in Outlook 2007](http://support.microsoft.com/kb/956070).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cfeca-125">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="cfeca-125">See also</span></span>



[<span data-ttu-id="cfeca-126">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cfeca-126">IPSTOVERRIDEREQ : IUnknown</span></span>](ipstoverridereqiunknown.md)

