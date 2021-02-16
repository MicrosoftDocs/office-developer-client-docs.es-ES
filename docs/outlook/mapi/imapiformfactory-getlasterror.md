---
title: IMAPIFormFactoryGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormFactory.GetLastError
api_type:
- COM
ms.assetid: 4b1d85f6-7996-4839-b985-abf83e305651
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 2c83f7788d9c01ab02f1a2bc39a35abe2c5a21c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417013"
---
# <a name="imapiformfactorygetlasterror"></a>IMAPIFormFactory::GetLastError

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve una [estructura MAPIERROR](mapierror.md) que contiene información sobre el error anterior que se produce en el objeto de fábrica de formularios. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parámetros

 _hResult_
  
> [entrada] Un tipo de datos HRESULT que contiene el valor de error generado en la llamada al método anterior.
    
 _ulFlags_
  
> [entrada] Máscara de bits de marcas que controla el tipo de cadenas devueltas. Se puede establecer la siguiente marca: 
    
MAPI_UNICODE 
  
> Las cadenas de la **estructura MAPIERROR** devueltas en el parámetro  _lppMAPIError_ están en formato Unicode. Si no MAPI_UNICODE marca, las cadenas están en formato ANSI. 
    
 _lppMAPIError_
  
> [salida] Puntero a un puntero a la estructura **MAPIERROR** devuelta que contiene información de versión, componente y contexto del error. Este parámetro se puede establecer en NULL si no hay ninguna **estructura MAPIERROR** que devolver. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_BAD_CHARWIDTH 
  
> Se estableció MAPI_UNICODE marca y **GetLastError** no admite Unicode o MAPI_UNICODE no se estableció **y GetLastError solo** admite Unicode. 
    
## <a name="remarks"></a>Comentarios

El **método IMAPIFormFactory::GetLastError** proporciona información acerca de una llamada de método anterior que ha fallado. Los autores de llamadas pueden proporcionar a sus usuarios información detallada sobre el error incluyendo los datos de la estructura **MAPIERROR** en un cuadro de diálogo. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Puede usar la estructura **MAPIERROR** a la que apunta el parámetro  _lppMAPIError_ si MAPI proporciona uno solo si **GetLastError** devuelve S_OK. A veces MAPI no puede determinar cuál fue el último error o no tiene nada más que informar sobre el error. En esta situación, se devuelve un puntero a NULL  _en lppMAPIError_ en su lugar. 
  
Para obtener más información acerca **del método GetLastError,** vea [El uso de errores extendidos.](mapi-extended-errors.md)
  
## <a name="see-also"></a>Consulte también



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIFormFactory : IUnknown](imapiformfactoryiunknown.md)

