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
ms.openlocfilehash: fa3f1d6339000fcc53e0ee22dafec4362e65ca7f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309621"
---
# <a name="ipersistmessagesave"></a><span data-ttu-id="20234-103">IPersistMessage::Save</span><span class="sxs-lookup"><span data-stu-id="20234-103">IPersistMessage::Save</span></span>

  
  
<span data-ttu-id="20234-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="20234-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="20234-105">Guarda un formulario revisado en el mensaje desde el que se cargó o creó.</span><span class="sxs-lookup"><span data-stu-id="20234-105">Saves a revised form back to the message from which it was loaded or created.</span></span>
  
```cpp
HRESULT Save(
  LPMESSAGE pMessage,
  ULONG fSameAsLoad
);
```

## <a name="parameters"></a><span data-ttu-id="20234-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="20234-106">Parameters</span></span>

 <span data-ttu-id="20234-107">_pMessage_</span><span class="sxs-lookup"><span data-stu-id="20234-107">_pMessage_</span></span>
  
> <span data-ttu-id="20234-108">[entrada] Puntero al mensaje.</span><span class="sxs-lookup"><span data-stu-id="20234-108">[in] A pointer to the message.</span></span>
    
 <span data-ttu-id="20234-109">_fSameAsLoad_</span><span class="sxs-lookup"><span data-stu-id="20234-109">_fSameAsLoad_</span></span>
  
> <span data-ttu-id="20234-110">[entrada] TRUE para indicar que el mensaje al que apunta  _pMessage_ es el mensaje desde el que se cargó o creó el formulario; de lo contrario, FALSE.</span><span class="sxs-lookup"><span data-stu-id="20234-110">[in] TRUE to indicate that the message pointed to by  _pMessage_ is the message from which the form was loaded or created; otherwise, FALSE.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="20234-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="20234-111">Return value</span></span>

<span data-ttu-id="20234-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="20234-112">S_OK</span></span> 
  
> <span data-ttu-id="20234-113">El formulario se guardó correctamente.</span><span class="sxs-lookup"><span data-stu-id="20234-113">The form was successfully saved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="20234-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="20234-114">Remarks</span></span>

<span data-ttu-id="20234-115">Los visores de formularios llaman al método **IPersistMessage::Save** para volver a guardar un formulario revisado en el mensaje desde el que se cargó o creó.</span><span class="sxs-lookup"><span data-stu-id="20234-115">Form viewers call the **IPersistMessage::Save** method to save a revised form back to the message from which it was loaded or created.</span></span> 
  
 <span data-ttu-id="20234-116">**Solo** se debe llamar a Save cuando el formulario está en su [estado Normal.](normal-state.md)</span><span class="sxs-lookup"><span data-stu-id="20234-116">**Save** should only be called when the form is in its [Normal](normal-state.md) state.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="20234-117">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="20234-117">Notes to implementers</span></span>

<span data-ttu-id="20234-118">No confirmar los cambios guardados; es el autor de la llamada quien debe confirmar los cambios.</span><span class="sxs-lookup"><span data-stu-id="20234-118">Do not commit the saved changes; it is up to the caller to commit the changes.</span></span> <span data-ttu-id="20234-119">Nunca realice cambios en las propiedades que pertenecen al mensaje del formulario excepto durante **la llamada guardar.**</span><span class="sxs-lookup"><span data-stu-id="20234-119">Never make changes to the properties that belong to the form's message except during the **Save** call.</span></span> 
  
<span data-ttu-id="20234-120">Si  _fSameAsLoad_ se establece en TRUE, puede guardar los cambios en el mensaje existente del formulario.</span><span class="sxs-lookup"><span data-stu-id="20234-120">If  _fSameAsLoad_ is set to TRUE, you can save the changes to the form's existing message.</span></span> <span data-ttu-id="20234-121">Si  _fSameAsLoad_ se establece en FALSE, debe copiar todas las propiedades del mensaje original en el mensaje al que apunta  _pMessage_ antes de realizar el guardado.</span><span class="sxs-lookup"><span data-stu-id="20234-121">If  _fSameAsLoad_ is set to FALSE, you must copy all of the properties from the original message into the message pointed to by  _pMessage_ before performing the save.</span></span> <span data-ttu-id="20234-122">Utilice el método [IMAPIProp::CopyTo](imapiprop-copyto.md) del mensaje original para copiar las propiedades.</span><span class="sxs-lookup"><span data-stu-id="20234-122">Use the original message's [IMAPIProp::CopyTo](imapiprop-copyto.md) method to copy the properties.</span></span> 
  
<span data-ttu-id="20234-123">Cuando se hayan copiado todas las propiedades, escriba el [estado NoScribable.](noscribble-state.md)</span><span class="sxs-lookup"><span data-stu-id="20234-123">When all of the properties have been copied, enter the [NoScribble](noscribble-state.md) state.</span></span> <span data-ttu-id="20234-124">Si no se produce ningún error, devuelva S_OK.</span><span class="sxs-lookup"><span data-stu-id="20234-124">If no errors occur, return S_OK.</span></span> <span data-ttu-id="20234-125">De lo contrario, devuelva el error de la acción con error.</span><span class="sxs-lookup"><span data-stu-id="20234-125">Otherwise, return the error from the failed action.</span></span> 
  
<span data-ttu-id="20234-126">Si **se** llama a Save cuando el formulario está en un estado distinto de Normal, E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="20234-126">If **Save** is called when the form is in any state other than Normal, return E_UNEXPECTED.</span></span> 
  
<span data-ttu-id="20234-127">Para obtener más información acerca de cómo guardar objetos de almacenamiento, consulte la documentación sobre los [métodos IPersistStorage.](https://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="20234-127">For more information about saving storage objects, see the documentation on the [IPersistStorage](https://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) methods.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="20234-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="20234-128">See also</span></span>



[<span data-ttu-id="20234-129">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="20234-129">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)


[<span data-ttu-id="20234-130">Estados de formulario</span><span class="sxs-lookup"><span data-stu-id="20234-130">Form States</span></span>](form-states.md)

