---
title: IMAPISupportGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.GetLastError
api_type:
- COM
ms.assetid: 5b4290d9-230f-416a-9644-188578565c7b
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 3e641842dd8264c0cd3556c498bd74c77bda32f7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577509"
---
# <a name="imapisupportgetlasterror"></a>IMAPISupport::GetLastError

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el error de objeto de soporte técnico anterior. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parámetros

 _hResult_
  
> [entrada] Un identificador para el valor de error generado en la llamada al método anterior para el objeto de soporte.
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla el tipo de cadenas devueltas. Se puede establecer la marca siguiente:
    
MAPI_UNICODE. 
  
> Las cadenas en la estructura **MAPIERROR** devuelta en el parámetro _lppMAPIError_ están en formato Unicode. Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI. 
    
 _lppMAPIError_
  
> [out] Un puntero a un puntero a la estructura **MAPIERROR** que contiene información de versión, el componente y el contexto para el error. El parámetro _lppMAPIError_ se puede establecer en NULL si no se puede proporcionar una estructura **MAPIERROR** con información de error apropiado. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelve el valor esperado o los valores.
    
MAPI_E_BAD_CHARWIDTH 
  
> Se ha establecido el indicador MAPI_UNICODE y MAPI no es compatible con Unicode, o bien, no se ha establecido MAPI_UNICODE y MAPI admite sólo Unicode.
    
## <a name="remarks"></a>Comentarios

El método **IMAPISupport::GetLastError** se implementa para todos los objetos de soporte técnico. Los autores de llamadas pueden proporcionar a sus usuarios con información detallada sobre el error mediante la inclusión de los datos de la estructura **MAPIERROR** en un cuadro de diálogo. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Puede usar el puntero a la estructura **MAPIERROR** , si MAPI proporciona uno, en el parámetro _lppMAPIError_ sólo si **GetLastError** devuelve S_OK. En ocasiones, MAPI no puede determinar cuál era el último error o no tiene nada más para informe sobre el error. En esta situación, _lppMAPIError_ devuelve un puntero a NULL en su lugar. 
  
Para obtener más información acerca del método **GetLastError** , vea [Errores de MAPI extendida](mapi-extended-errors.md).
  
Para liberar toda la memoria asignada por MAPI, llame a la función [MAPIFreeBuffer](mapifreebuffer.md) para la estructura **MAPIERROR** devuelta. 
  
## <a name="see-also"></a>Recursos adicionales



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


[MAPI extendida de errores](mapi-extended-errors.md)

