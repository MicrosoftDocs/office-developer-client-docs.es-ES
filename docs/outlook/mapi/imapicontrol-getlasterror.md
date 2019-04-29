---
title: IMAPIControlGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIControl.GetLastError
api_type:
- COM
ms.assetid: 83290b8e-fffc-41c8-a01e-578d130b65c5
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 10ac4e33b3f734ec2ce3205aa1897e0418cb563d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421154"
---
# <a name="imapicontrolgetlasterror"></a>IMAPIControl::GetLastError

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el error de control de botón anterior. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parameters

 _Valores_
  
> a Identificador del valor de error generado en la llamada al método anterior.
    
 _ulFlags_
  
> a Máscara de máscara de marcadores que controla el tipo de las cadenas devueltas. Se puede establecer la siguiente marca:
    
MAPI_UNICODE 
  
> Las cadenas de la estructura **MAPIERROR** devueltas en el parámetro _lppMAPIError_ están en formato Unicode. Si no se establece la marca MAPI_UNICODE, las cadenas están en formato ANSI. 
    
 _lppMAPIError_
  
> contempla Un puntero a un puntero a una estructura **MAPIERROR** que contiene información sobre la versión, el componente y el contexto del error. El parámetro _lppMAPIError_ puede establecerse en NULL si el proveedor no puede proporcionar una estructura **MAPIERROR** con la información adecuada. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_BAD_CHARWIDTH 
  
> Se estableció la marca MAPI_UNICODE y la implementación no admite Unicode, o no se estableció MAPI_UNICODE y la implementación solo admite Unicode.
    
## <a name="remarks"></a>Comentarios

Los proveedores de servicios implementan el método **IMAPIControl:: GetLastError** para proporcionar información sobre una llamada a un método anterior que no se ha realizado correctamente. MAPI puede proporcionar a los usuarios información detallada sobre el error al mostrar los datos de la estructura **MAPIERROR** en un mensaje o cuadro de diálogo. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

No es necesario tener información que incluir en la estructura **MAPIERROR** para cada error. Puede que no sea posible determinar cuál era el error anterior. Si tiene información, devuelva S_OK y los datos adecuados en la estructura **MAPIERROR** . Si no hay información disponible, devuelva S_OK y un puntero a NULL para el parámetro _lppMAPIError_ . 
  
Para obtener más información sobre el método **GetLastError** , vea [errores extendidos de MAPI](mapi-extended-errors.md).
  
## <a name="see-also"></a>Ver también



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIControl : IUnknown](imapicontroliunknown.md)

