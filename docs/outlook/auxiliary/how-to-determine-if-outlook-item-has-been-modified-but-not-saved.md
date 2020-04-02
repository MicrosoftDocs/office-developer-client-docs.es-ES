---
title: Determinar si un elemento de Outlook se ha modificado pero no guardado (referencia auxiliar de Outlook)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 65fba557-5fb0-42de-8715-eccda1f3c648
description: En este tema se muestra cómo utilizar el identificador de envío dispidFDirty para invocar la propiedad correspondiente en un elemento de Outlook para ver si el elemento se ha modificado y no se ha guardado.
ms.openlocfilehash: 5dc20a45342e0434ab19d7c2347e98dec27b61b8
ms.sourcegitcommit: 007aa2ceb4f569201c3f4372de5c83b6c61f8875
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/02/2020
ms.locfileid: "43102950"
---
# <a name="determine-if-an-outlook-item-has-been-modified-but-not-saved-outlook-auxiliary-reference"></a><span data-ttu-id="ce282-103">Determinar si un elemento de Outlook se ha modificado pero no guardado (referencia auxiliar de Outlook)</span><span class="sxs-lookup"><span data-stu-id="ce282-103">Determine if an Outlook item has been modified but not saved (Outlook Auxiliary Reference)</span></span>

<span data-ttu-id="ce282-104">En este tema se muestra cómo utilizar el identificador de envío **dispidFDirty** para invocar la propiedad correspondiente en un elemento de Outlook para ver si el elemento se ha modificado y no se ha guardado.</span><span class="sxs-lookup"><span data-stu-id="ce282-104">This topic shows how to use the **dispidFDirty** dispatch ID to invoke the corresponding property on an Outlook item, to see whether the item has been modified and has not been saved.</span></span> 
  
<span data-ttu-id="ce282-105">Dado un objeto de elemento, puede utilizar el método [IUnknown::QueryInterface](https://docs.microsoft.com/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para obtener un puntero de interfaz [IDispatch](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="ce282-105">Given an item object, you can use the [IUnknown::QueryInterface](https://docs.microsoft.com/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method to obtain an [IDispatch](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) interface pointer.</span></span> <span data-ttu-id="ce282-106">La función del tema `FIsItemDirty` acepta un puntero **IDispatch** , _pdisp_, como un parámetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="ce282-106">The function in the topic `FIsItemDirty` accepts an **IDispatch** pointer,  _pdisp_, as an input parameter.</span></span>  <span data-ttu-id="ce282-107">`FIsItemDirty` llama al método de [IDispatch:: Invoke](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) , especifique **dispidFDirty** como el argumento para el parámetro  _dispIdMember_ y el  `DISPATCH_METHOD | DISPATCH_PROPERTYGET` de marcadores de  _wFlags_, para comprobar si se ha modificado el elemento.</span><span class="sxs-lookup"><span data-stu-id="ce282-107">`FIsItemDirty` calls the [IDispatch::Invoke](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) method, specifying **dispidFDirty** as the argument for the  _dispIdMember_ parameter, and the flags  `DISPATCH_METHOD | DISPATCH_PROPERTYGET` for  _wFlags_, to verify whether the item has been modified.</span></span>  <span data-ttu-id="ce282-108">`FIsItemDirty`Devuelve un valor booleano (**true** para indicar que el elemento tiene cambios sin guardar; de lo contrario, **false**).</span><span class="sxs-lookup"><span data-stu-id="ce282-108">`FIsItemDirty` returns a Boolean value (**True** to indicate that the item has unsaved changes; otherwise, **False**).</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="ce282-109">Vea también</span><span class="sxs-lookup"><span data-stu-id="ce282-109">See also</span></span>

- [<span data-ttu-id="ce282-110">Constantes (API exportadas de Outlook)</span><span class="sxs-lookup"><span data-stu-id="ce282-110">Constants (Outlook exported APIs)</span></span>](constants-outlook-exported-apis.md)

