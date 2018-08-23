---
title: Determinar si un elemento de Outlook se ha modificado pero no se ha guardado (referencia auxiliar de Outlook)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 65fba557-5fb0-42de-8715-eccda1f3c648
description: En este tema se muestra cómo utilizar el identificador de envío dispidFDirty para invocar la propiedad correspondiente en un elemento de Outlook para ver si el elemento se ha modificado y no se ha guardado.
ms.openlocfilehash: adaa0f72d427a5cfc98b93e8aa4403d5a76ecd9d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588100"
---
# <a name="determine-if-an-outlook-item-has-been-modified-but-not-saved-outlook-auxiliary-reference"></a>Determinar si un elemento de Outlook se ha modificado pero no se ha guardado (referencia auxiliar de Outlook)

En este tema se muestra cómo utilizar el identificador de envío **dispidFDirty** para invocar la propiedad correspondiente en un elemento de Outlook para ver si el elemento se ha modificado y no se ha guardado. 
  
Dado un objeto de elemento, puede utilizar el método [IUnknown::QueryInterface](https://docs.microsoft.com/en-us/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)) para obtener un puntero de interfaz [IDispatch](https://docs.microsoft.com/en-us/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) . La función en el tema `FIsItemDirty` acepta un puntero **IDispatch** , _pdisp_, como un parámetro de entrada.  `FIsItemDirty` llama al método de [IDispatch:: Invoke](https://docs.microsoft.com/en-us/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) , especifique **dispidFDirty** como el argumento para el parámetro  _dispIdMember_ y el  `DISPATCH_METHOD | DISPATCH_PROPERTYGET` de marcadores de  _wFlags_, para comprobar si se ha modificado el elemento.  `FIsItemDirty`Devuelve un valor booleano (**True** para indicar que el elemento no se han guardado los cambios; en caso contrario, **False**).
  
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

## <a name="see-also"></a>Recursos adicionales

- [Constantes (API exportadas de Outlook)](constants-outlook-exported-apis.md)

