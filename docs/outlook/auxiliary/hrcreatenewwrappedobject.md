---
title: HrCreateNewWrappedObject
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 780ade1c-88d0-04d2-ba7e-251c19c43438
description: Crea un objeto que puede tener acceso un cliente en un formato de carácter preferido.
ms.openlocfilehash: 187bcbce8fd1170e05f57c5c9147a8962669fea4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816073"
---
# <a name="hrcreatenewwrappedobject"></a>HrCreateNewWrappedObject

Crea un objeto que puede tener acceso un cliente en un formato de carácter preferido.
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Exportada por:  <br/> |Msmapi32.dll  <br/> |
|Llamado por:  <br/> |Cliente  <br/> |
|Se implementa mediante:  <br/> |Outlook  <br/> |
   
```cpp
HRESULT HrCreateNewWrappedObject( 
    LPVOID        pvUnwrapped, 
    ULONG         ulUnwrappedFlags, 
    ULONG         ulWrappedFlags, 
    const IID     *pIID, 
    const ULONG   *pulReserved, 
    BOOL          fCheckWrap, 
    LPVOID       *ppvWrapped 
);

```

## <a name="parameters"></a>Parámetros

_pvUnwrapped_
  
> [entrada] El objeto de Outlook no ajustado inicial. Debe implementar una de las interfaces siguientes:
    
   - [IMailUser: IMAPIProp](http://msdn.microsoft.com/library/74c25870-62d9-484a-9a99-4dc35c52479e%28Office.15%29.aspx), [IMAPIFolder: IMAPIContainer](http://msdn.microsoft.com/library/bc2e8d17-7687-43c2-8f01-b677703f7288%28Office.15%29.aspx), [IMessage: IMAPIProp](http://msdn.microsoft.com/library/7e244d40-595e-432c-aa8c-f9f62ca3c138%28Office.15%29.aspx), [IMsgStore: IMAPIProp](http://msdn.microsoft.com/library/20090114-b183-4767-8971-a304a9aa47e6%28Office.15%29.aspx), [IMSLogon: IUnknown](http://msdn.microsoft.com/library/d87093dc-f705-465f-ab3c-944ca0cd3e54%28Office.15%29.aspx), o [IOSTX](http://msdn.microsoft.com/library/f374d8d9-be8e-2489-d5fe-8a92e0ecfc6f%28Office.15%29.aspx).
    
_ulUnwrappedFlags_
  
> [entrada] Marcas que caracterizan el objeto inicial no ajustado. Debe ser uno o varios de los siguientes valores:
    
   - DDLWRAP_FLAG_ANSI: objeto Unwrapped es ANSI.
    
   - DDLWRAP_FLAG_UNICODE: objeto Unwrapped es UNICODE.
    
_ulWrappedFlags_
  
>  [entrada] Marcas para el formato de carácter preferido. Debe ser uno o varios de los siguientes valores: 
    
   - DDLWRAP_FLAG_ANSI: objeto Wrapped se mostrarán como ANSI.
    
   - DDLWRAP_FLAG_UNICODE: objeto Wrapped se mostrarán como UNICODE.
    
_pIID_
  
>  [entrada] El identificador de la interfaz admitido por el objeto no ajustado; establecer en NULL si esto es desconocido. 
    
_pulReserved_
  
>  [entrada] Este parámetro no se usa. Debe ser NULL. 
    
_fCheckWrap_
  
>  [entrada] Establezca este parámetro en **true** si se deben comprobar _pvUnwrapped_ para su formato antes del ajuste; establézcalo en **false** si el objeto se debe ajustar sin comprobar. 
    
_ppvWrapped_
  
>  [out] Un puntero al objeto solicitado, ajustado en el formato de caracteres solicitado. 
    
## <a name="return-values"></a>Valores devueltos

S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.
  
## <a name="remarks"></a>Notas

Pasar un objeto ajustado con _fCheckWrap_ establecido en **true** , se producirá un objeto no ajustado. Independientemente de si se ajusta el objeto devuelto, el cliente es responsable de liberar la referencia en el objeto devuelto. 
  
Cuando se usa **GetProcAddress** para buscar la dirección de esta función en msmapi32.dll, especifique **HrCreateNewWrappedObject@28** como el nombre del procedimiento. 
  
## <a name="see-also"></a>Vea también

- [Acerca de la capa de degradación de datos API](about-the-data-degradation-layer-api.md)
- [Constantes (capa de degradación de datos API)](constants-data-degradation-layer-api.md)

