---
title: IPersistMessageSave
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.Save
api_type:
- COM
ms.assetid: 17875c13-f55b-4538-ac6f-c020281c3175
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 222d8257a802739ee8e513a0ea95a13f4b99322e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817867"
---
# <a name="ipersistmessagesave"></a><span data-ttu-id="09a8a-103">IPersistMessage::Save</span><span class="sxs-lookup"><span data-stu-id="09a8a-103">IPersistMessage::Save</span></span>

  
  
<span data-ttu-id="09a8a-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="09a8a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="09a8a-105">Guarda un formulario revisado el mensaje desde la que se ha cargado o creado.</span><span class="sxs-lookup"><span data-stu-id="09a8a-105">Saves a revised form back to the message from which it was loaded or created.</span></span>
  
```cpp
HRESULT Save(
  LPMESSAGE pMessage,
  ULONG fSameAsLoad
);
```

## <a name="parameters"></a><span data-ttu-id="09a8a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="09a8a-106">Parameters</span></span>

 <span data-ttu-id="09a8a-107">_pMessage_</span><span class="sxs-lookup"><span data-stu-id="09a8a-107">_pMessage_</span></span>
  
> <span data-ttu-id="09a8a-108">[entrada] Un puntero al mensaje.</span><span class="sxs-lookup"><span data-stu-id="09a8a-108">[in] A pointer to the message.</span></span>
    
 <span data-ttu-id="09a8a-109">_fSameAsLoad_</span><span class="sxs-lookup"><span data-stu-id="09a8a-109">_fSameAsLoad_</span></span>
  
> <span data-ttu-id="09a8a-110">[entrada] TRUE para indicar que el mensaje que apunta por _pMessage_ es el mensaje desde la que el formulario se ha cargado o creado; en caso contrario, es FALSE.</span><span class="sxs-lookup"><span data-stu-id="09a8a-110">[in] TRUE to indicate that the message pointed to by  _pMessage_ is the message from which the form was loaded or created; otherwise, FALSE.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="09a8a-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="09a8a-111">Return value</span></span>

<span data-ttu-id="09a8a-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="09a8a-112">S_OK</span></span> 
  
> <span data-ttu-id="09a8a-113">El formulario se ha guardado correctamente.</span><span class="sxs-lookup"><span data-stu-id="09a8a-113">The form was successfully saved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="09a8a-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="09a8a-114">Remarks</span></span>

<span data-ttu-id="09a8a-115">Visores de formulario llamar al método **IPersistMessage::Save** para guardar un formulario revisado en el mensaje desde la que se ha cargado o creado.</span><span class="sxs-lookup"><span data-stu-id="09a8a-115">Form viewers call the **IPersistMessage::Save** method to save a revised form back to the message from which it was loaded or created.</span></span> 
  
 <span data-ttu-id="09a8a-116">**Guardar** sólo se debe llamar cuando el formulario está en su estado [Normal](normal-state.md) .</span><span class="sxs-lookup"><span data-stu-id="09a8a-116">**Save** should only be called when the form is in its [Normal](normal-state.md) state.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="09a8a-117">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="09a8a-117">Notes to implementers</span></span>

<span data-ttu-id="09a8a-118">No confirme los cambios guardados; es el autor de la llamada para confirmar los cambios.</span><span class="sxs-lookup"><span data-stu-id="09a8a-118">Do not commit the saved changes; it is up to the caller to commit the changes.</span></span> <span data-ttu-id="09a8a-119">Nunca realice cambios en las propiedades que pertenecen al mensaje del formulario, excepto durante la llamada de **Guardar** .</span><span class="sxs-lookup"><span data-stu-id="09a8a-119">Never make changes to the properties that belong to the form's message except during the **Save** call.</span></span> 
  
<span data-ttu-id="09a8a-120">Si _fSameAsLoad_ está establecida en TRUE, puede guardar los cambios al mensaje existente del formulario.</span><span class="sxs-lookup"><span data-stu-id="09a8a-120">If  _fSameAsLoad_ is set to TRUE, you can save the changes to the form's existing message.</span></span> <span data-ttu-id="09a8a-121">Si _fSameAsLoad_ está establecida en FALSE, debe copiar todas las propiedades del mensaje original en el mensaje que apunta _pMessage_ antes de realizar la operación de guardar.</span><span class="sxs-lookup"><span data-stu-id="09a8a-121">If  _fSameAsLoad_ is set to FALSE, you must copy all of the properties from the original message into the message pointed to by  _pMessage_ before performing the save.</span></span> <span data-ttu-id="09a8a-122">Utilice el método de [IMAPIProp::CopyTo](imapiprop-copyto.md) del mensaje original para copiar las propiedades.</span><span class="sxs-lookup"><span data-stu-id="09a8a-122">Use the original message's [IMAPIProp::CopyTo](imapiprop-copyto.md) method to copy the properties.</span></span> 
  
<span data-ttu-id="09a8a-123">Cuando todas las propiedades se han copiado, especifique el estado de [NoScribble](noscribble-state.md) .</span><span class="sxs-lookup"><span data-stu-id="09a8a-123">When all of the properties have been copied, enter the [NoScribble](noscribble-state.md) state.</span></span> <span data-ttu-id="09a8a-124">Si no se producen errores, devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="09a8a-124">If no errors occur, return S_OK.</span></span> <span data-ttu-id="09a8a-125">De lo contrario, devolverá el error de la acción con errores.</span><span class="sxs-lookup"><span data-stu-id="09a8a-125">Otherwise, return the error from the failed action.</span></span> 
  
<span data-ttu-id="09a8a-126">Si se llama a **Guardar** cuando el formulario está en cualquier estado que no sea Normal, devolver E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="09a8a-126">If **Save** is called when the form is in any state other than Normal, return E_UNEXPECTED.</span></span> 
  
<span data-ttu-id="09a8a-127">Para obtener más información acerca de cómo guardar objetos de almacenamiento, consulte la documentación sobre los métodos [IPersistStorage](http://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="09a8a-127">For more information about saving storage objects, see the documentation on the [IPersistStorage](http://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) methods.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="09a8a-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="09a8a-128">See also</span></span>



[<span data-ttu-id="09a8a-129">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="09a8a-129">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)


[<span data-ttu-id="09a8a-130">Estados de formulario</span><span class="sxs-lookup"><span data-stu-id="09a8a-130">Form States</span></span>](form-states.md)

