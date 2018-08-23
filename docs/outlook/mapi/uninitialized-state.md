---
title: Estado sin inicializar
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e071b50f-2e75-4537-ac7b-4a2f5ebea83d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 95ed80a6d0ea6a6a7c8cc768b32981ac899b69e4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578251"
---
# <a name="uninitialized-state"></a><span data-ttu-id="b644c-103">Estado sin inicializar</span><span class="sxs-lookup"><span data-stu-id="b644c-103">Uninitialized State</span></span>

  
  
<span data-ttu-id="b644c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b644c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b644c-105">El estado no inicializado es el formulario de estado inicial objetos deberían estar en cuando se crea por primera vez.</span><span class="sxs-lookup"><span data-stu-id="b644c-105">The Uninitialized state is the initial state form objects should be in when they are first created.</span></span> <span data-ttu-id="b644c-106">Objetos de formulario se convierten en inicializar con datos de mensaje cuando una aplicación cliente llama al método [IPersistMessage::InitNew](ipersistmessage-initnew.md) o [IPersistMessage::Load](ipersistmessage-load.md) en el objeto de formulario.</span><span class="sxs-lookup"><span data-stu-id="b644c-106">Form objects become initialized with message data when a client application calls the [IPersistMessage::InitNew](ipersistmessage-initnew.md) or [IPersistMessage::Load](ipersistmessage-load.md) method on the form object.</span></span> <span data-ttu-id="b644c-107">La siguiente tabla describe las transiciones permitidas desde el estado Unitialized.</span><span class="sxs-lookup"><span data-stu-id="b644c-107">The following table describes allowed transitions from the Unitialized state.</span></span> 
  
|<span data-ttu-id="b644c-108">**IPersistMessage (método)**</span><span class="sxs-lookup"><span data-stu-id="b644c-108">**IPersistMessage method**</span></span>|<span data-ttu-id="b644c-109">**Acción**</span><span class="sxs-lookup"><span data-stu-id="b644c-109">**Action**</span></span>|<span data-ttu-id="b644c-110">**Nuevo estado**</span><span class="sxs-lookup"><span data-stu-id="b644c-110">**New state**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b644c-111">IPersistMessage::InitNew</span><span class="sxs-lookup"><span data-stu-id="b644c-111">IPersistMessage::InitNew</span></span>](ipersistmessage-initnew.md) <br/> |<span data-ttu-id="b644c-112">Cargar el objeto de formulario con los datos predeterminados.</span><span class="sxs-lookup"><span data-stu-id="b644c-112">Load the form object with default data.</span></span>  <br/> |[<span data-ttu-id="b644c-113">Normal</span><span class="sxs-lookup"><span data-stu-id="b644c-113">Normal</span></span>](normal-state.md) <br/> |
|[<span data-ttu-id="b644c-114">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="b644c-114">IPersistMessage::Load</span></span>](ipersistmessage-load.md) <br/> |<span data-ttu-id="b644c-115">Cargar el objeto de formulario con datos desde el mensaje de destino.</span><span class="sxs-lookup"><span data-stu-id="b644c-115">Load the form object with data from the target message.</span></span>  <br/> |<span data-ttu-id="b644c-116">Importance</span><span class="sxs-lookup"><span data-stu-id="b644c-116">Normal</span></span>  <br/> |
|[<span data-ttu-id="b644c-117">IPersistMessage::GetClassID</span><span class="sxs-lookup"><span data-stu-id="b644c-117">IPersistMessage::GetClassID</span></span>](ipersistmessage-getclassid.md) <br/> |<span data-ttu-id="b644c-118">Devolver un resultado correcto, o establece el último error y devolver E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="b644c-118">Return success, or set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="b644c-119">No inicializado</span><span class="sxs-lookup"><span data-stu-id="b644c-119">Uninitialized</span></span>  <br/> |
|[<span data-ttu-id="b644c-120">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="b644c-120">IPersistMessage::GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="b644c-121">Devolver el último error.</span><span class="sxs-lookup"><span data-stu-id="b644c-121">Return the last error.</span></span>  <br/> |<span data-ttu-id="b644c-122">No inicializado</span><span class="sxs-lookup"><span data-stu-id="b644c-122">Uninitialized</span></span>  <br/> |
|<span data-ttu-id="b644c-123">Otros [IPersistMessage: IUnknown](ipersistmessageiunknown.md) métodos o métodos de otras interfaces</span><span class="sxs-lookup"><span data-stu-id="b644c-123">Other [IPersistMessage : IUnknown](ipersistmessageiunknown.md) methods or methods from other interfaces</span></span>  <br/> |<span data-ttu-id="b644c-124">Establece el último error y devolver E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="b644c-124">Set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="b644c-125">No inicializado</span><span class="sxs-lookup"><span data-stu-id="b644c-125">Uninitialized</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b644c-126">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="b644c-126">See also</span></span>



[<span data-ttu-id="b644c-127">Estado normal</span><span class="sxs-lookup"><span data-stu-id="b644c-127">Normal State</span></span>](normal-state.md)
  
[<span data-ttu-id="b644c-128">Estados de formulario</span><span class="sxs-lookup"><span data-stu-id="b644c-128">Form States</span></span>](form-states.md)

