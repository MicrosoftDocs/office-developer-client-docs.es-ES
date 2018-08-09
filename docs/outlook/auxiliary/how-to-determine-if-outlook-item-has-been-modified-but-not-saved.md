---
title: Determinar si un elemento de Outlook se ha modificado pero no se ha guardado (referencia auxiliar de Outlook)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 65fba557-5fb0-42de-8715-eccda1f3c648
description: En este tema se muestra cómo utilizar el identificador de envío dispidFDirty para invocar la propiedad correspondiente en un elemento de Outlook para ver si el elemento se ha modificado y no se ha guardado.
ms.openlocfilehash: ece6ede368cf2ffb3b18575161fef4b3f132fdf0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816069"
---
# <a name="determine-if-an-outlook-item-has-been-modified-but-not-saved-outlook-auxiliary-reference"></a><span data-ttu-id="23e29-103">Determinar si un elemento de Outlook se ha modificado pero no se ha guardado (referencia auxiliar de Outlook)</span><span class="sxs-lookup"><span data-stu-id="23e29-103">Determine if an Outlook item has been modified but not saved (Outlook Auxiliary Reference)</span></span>

<span data-ttu-id="23e29-104">En este tema se muestra cómo utilizar el identificador de envío **dispidFDirty** para invocar la propiedad correspondiente en un elemento de Outlook para ver si el elemento se ha modificado y no se ha guardado.</span><span class="sxs-lookup"><span data-stu-id="23e29-104">This topic shows how to use the **dispidFDirty** dispatch ID to invoke the corresponding property on an Outlook item, to see whether the item has been modified and has not been saved.</span></span> 
  
<span data-ttu-id="23e29-105">Dado un objeto de elemento, puede utilizar el método [IUnknown::QueryInterface](http://msdn.microsoft.com/library/com.iunknown_queryinterface.aspx) para obtener un puntero de interfaz [IDispatch](http://msdn.microsoft.com/library/ebbff4bc-36b2-4861-9efa-ffa45e013eb5%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="23e29-105">Given an item object, you can use the [IUnknown::QueryInterface](http://msdn.microsoft.com/library/com.iunknown_queryinterface.aspx) method to obtain an [IDispatch](http://msdn.microsoft.com/library/ebbff4bc-36b2-4861-9efa-ffa45e013eb5%28Office.15%29.aspx) interface pointer.</span></span> <span data-ttu-id="23e29-106">La función en el tema `FIsItemDirty` acepta un puntero **IDispatch** , _pdisp_, como un parámetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="23e29-106">The function in the topic `FIsItemDirty` accepts an **IDispatch** pointer,  _pdisp_, as an input parameter.</span></span>  <span data-ttu-id="23e29-107">`FIsItemDirty` llama al método de [IDispatch:: Invoke](http://msdn.microsoft.com/library/964ade8e-9d8a-4d32-bd47-aa678912a54d%28Office.15%29.aspx) , especifique **dispidFDirty** como el argumento para el parámetro  _dispIdMember_ y el  `DISPATCH_METHOD | DISPATCH_PROPERTYGET` de marcadores de  _wFlags_, para comprobar si se ha modificado el elemento.</span><span class="sxs-lookup"><span data-stu-id="23e29-107">`FIsItemDirty` calls the [IDispatch::Invoke](http://msdn.microsoft.com/library/964ade8e-9d8a-4d32-bd47-aa678912a54d%28Office.15%29.aspx) method, specifying **dispidFDirty** as the argument for the  _dispIdMember_ parameter, and the flags  `DISPATCH_METHOD | DISPATCH_PROPERTYGET` for  _wFlags_, to verify whether the item has been modified.</span></span>  <span data-ttu-id="23e29-108">`FIsItemDirty`Devuelve un valor booleano (**True** para indicar que el elemento no se han guardado los cambios; en caso contrario, **False**).</span><span class="sxs-lookup"><span data-stu-id="23e29-108">`FIsItemDirty` returns a Boolean value (**True** to indicate that the item has unsaved changes; otherwise, **False**).</span></span>
  
```cpp
bool FIsItemDirty(IDispatch *pdisp)
{
    DISPPARAMS dispparams;
    UINT uArgErr;
    HRESULT hr = S_OK;
    CComVariant varDirty;
    dispparams.rgvarg = 0;
    dispparams.cArgs = 0;
    dispparams.cNamedArgs = 0;
    dispparams.rgdispidNamedArgs = NULL;
    hr = pdisp->Invoke(dispidFDirty,
        IID_NULL,
        LOCALE_SYSTEM_DEFAULT,
        DISPATCH_METHOD | DISPATCH_PROPERTYGET,
        &amp;dispparams,
        &amp;varDirty,
        NULL,
        &amp;uArgErr);
    return SUCCEEDED(hr) &amp;&amp; varDirty.bVal;
}

```

## <a name="see-also"></a><span data-ttu-id="23e29-109">Vea también</span><span class="sxs-lookup"><span data-stu-id="23e29-109">See also</span></span>

- [<span data-ttu-id="23e29-110">Constantes (API exportadas de Outlook)</span><span class="sxs-lookup"><span data-stu-id="23e29-110">Constants (Outlook exported APIs)</span></span>](constants-outlook-exported-apis.md)

