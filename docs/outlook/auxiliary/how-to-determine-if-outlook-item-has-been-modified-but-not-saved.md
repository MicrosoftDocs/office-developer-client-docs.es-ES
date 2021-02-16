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
# <a name="determine-if-an-outlook-item-has-been-modified-but-not-saved-outlook-auxiliary-reference"></a>Determinar si un elemento de Outlook se ha modificado pero no guardado (referencia auxiliar de Outlook)

En este tema se muestra cómo utilizar el identificador de envío **dispidFDirty** para invocar la propiedad correspondiente en un elemento de Outlook para ver si el elemento se ha modificado y no se ha guardado. 
  
Dado un objeto de elemento, puede utilizar el método [IUnknown::QueryInterface](https://docs.microsoft.com/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para obtener un puntero de interfaz [IDispatch](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) . La función del tema `FIsItemDirty` acepta un puntero **IDispatch,**  _pdisp_, como parámetro de entrada.  `FIsItemDirty` llama al método de [IDispatch:: Invoke](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) , especifique **dispidFDirty** como el argumento para el parámetro  _dispIdMember_ y el  `DISPATCH_METHOD | DISPATCH_PROPERTYGET` de marcadores de  _wFlags_, para comprobar si se ha modificado el elemento.  `FIsItemDirty` devuelve un valor booleano (**True** para indicar que el elemento tiene cambios sin guardar; de lo contrario, **False**).
  
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

## <a name="see-also"></a>Consulte también

- [Constantes (API exportadas de Outlook)](constants-outlook-exported-apis.md)

