---
title: IMAPIViewContextGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.GetLastError
api_type:
- COM
ms.assetid: 3306e37a-2500-4281-96c3-ca0d5c81909d
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: bcd8e977d924bae170dcad27c672b963189cfa94
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351403"
---
# <a name="imapiviewcontextgetlasterror"></a>IMAPIViewContext::GetLastError

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el error anterior que se produce en el objeto de contexto de vista. 
  
```cpp
HRESULT GetLastError(
HRESULT hResult,
ULONG ulFlags,
LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parameters

 _Valores_
  
> a Tipo de datos HRESULT que contiene el valor de error generado en la llamada al método anterior.
    
 _ulFlags_
  
> a Máscara de máscara de los marcadores que controla el tipo de cadenas devueltas. Se puede establecer la siguiente marca:
    
MAPI_UNICODE 
  
> Las cadenas de la estructura **MAPIERROR** devueltas en el parámetro _lppMAPIError_ están en formato Unicode. Si no se establece la marca MAPI_UNICODE, las cadenas están en formato ANSI. 
    
 _lppMAPIError_
  
> contempla Puntero a un puntero a la estructura **MAPIERROR** devuelta que contiene la información de versión, componente y contexto del error. Este parámetro se puede establecer en NULL si no hay ninguna estructura **MAPIERROR** para devolver. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_BAD_CHARWIDTH 
  
> Se estableció la marca MAPI_UNICODE y **GetLastError** no admite Unicode, o bien no se estableció MAPI_UNICODE y **GetLastError** solo admite Unicode. 
    
## <a name="remarks"></a>Comentarios

El método **IMAPIViewContext:: GetLastError** proporciona información sobre una llamada a un método anterior que produjo un error. Los autores de llamadas pueden proporcionar a sus usuarios información detallada acerca del error al incluir los datos de la estructura **MAPIERROR** en un cuadro de diálogo. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Puede hacer uso de la estructura **MAPIERROR** apuntado por el parámetro _lppMAPIError_ si MAPI proporciona solo una si **GetLastError** Devuelve S_OK. A veces MAPI no puede determinar el último error o no tiene nada más para informar sobre el error. En esta situación, un puntero a NULL se devuelve en _lppMAPIError_ en su lugar. 
  
Para obtener más información sobre el método **GetLastError** , vea [errores extendidos de MAPI](mapi-extended-errors.md).
  
## <a name="see-also"></a>Vea también



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)

