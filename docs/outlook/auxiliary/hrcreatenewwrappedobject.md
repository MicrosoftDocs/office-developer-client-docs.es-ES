---
title: HrCreateNewWrappedObject
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 780ade1c-88d0-04d2-ba7e-251c19c43438
description: Crea un objeto al que un cliente puede tener acceso en un formato de carácter preferido.
ms.openlocfilehash: 3f68e0f275bcc5df065b3113d3322d6957f76df0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317608"
---
# <a name="hrcreatenewwrappedobject"></a>HrCreateNewWrappedObject

Crea un objeto al que un cliente puede tener acceso en un formato de carácter preferido.
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Exportada por:  <br/> |msmapi32.dll  <br/> |
|Llamado por:  <br/> |Cliente  <br/> |
|Implementado por:  <br/> |Outlook  <br/> |
   
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

## <a name="parameters"></a>Parameters

_pvUnwrapped_
  
> [in] El objeto Outlook inicial sin envolver. Debe implementar una de las interfaces siguientes:
    
   - [IMailUser : IMAPIProp](https://msdn.microsoft.com/library/74c25870-62d9-484a-9a99-4dc35c52479e%28Office.15%29.aspx), [IMAPIFolder : IMAPIContainer](https://msdn.microsoft.com/library/bc2e8d17-7687-43c2-8f01-b677703f7288%28Office.15%29.aspx), [IMessage : IMAPIProp](https://msdn.microsoft.com/library/7e244d40-595e-432c-aa8c-f9f62ca3c138%28Office.15%29.aspx), [IMsgStore : IMAPIProp](https://msdn.microsoft.com/library/20090114-b183-4767-8971-a304a9aa47e6%28Office.15%29.aspx), [IMSLogon : IUnknown](https://msdn.microsoft.com/library/d87093dc-f705-465f-ab3c-944ca0cd3e54%28Office.15%29.aspx)o [IOSTX](https://msdn.microsoft.com/library/f374d8d9-be8e-2489-d5fe-8a92e0ecfc6f%28Office.15%29.aspx).
    
_ulUnwrappedFlags_
  
> [in] Marcas que caracterizan el objeto inicial sin envolver. Debe ser uno o varios de los siguientes valores:
    
   - DDLWRAP_FLAG_ANSI: el objeto Unwrapped es ANSI.
    
   - DDLWRAP_FLAG_UNICODE: el objeto Unwrapped es UNICODE.
    
_ulWrappedFlags_
  
>  [in] Marcas para el formato de carácter preferido. Debe ser uno o varios de los siguientes valores: 
    
   - DDLWRAP_FLAG_ANSI: el objeto Wrapped se expone como ANSI.
    
   - DDLWRAP_FLAG_UNICODE: el objeto Wrapped se expone como UNICODE.
    
_pIID_
  
>  [in] El identificador de la interfaz admitida por el objeto sin envolver; esta opción se establece en NULL si se desconoce. 
    
_pulReserved_
  
>  [in] Este parámetro no se usa. Debe ser NULL. 
    
_fCheckWrap_
  
>  [in] Establezca este parámetro en **true** si se debe comprobar el formato de  _pvUnwrapped_ antes de ajustarlo; establecerlo en **false** si el objeto debe ajustarse sin comprobarlo. 
    
_ppvWrapped_
  
>  [salida] Puntero al objeto solicitado, ajustado en el formato de carácter solicitado. 
    
## <a name="return-values"></a>Valores devueltos

S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.
  
## <a name="remarks"></a>Comentarios

Si se pasa un objeto ajustado con  _fCheckWrap_ establecido en **true,** se dará como resultado un objeto sin envolver. Independientemente de si el objeto devuelto está ajustado o no, el cliente es responsable de liberar la referencia en el objeto devuelto. 
  
Al usar **GetProcAddress para** buscar la dirección de esta función en msmapi32.dll, especifique **HrCreateNewWrappedObject@28** como el nombre del procedimiento. 
  
## <a name="see-also"></a>Vea también

- [Acerca de la capa de degradación de datos API](about-the-data-degradation-layer-api.md)
- [Constantes (API de capa de degradación de datos)](constants-data-degradation-layer-api.md)

