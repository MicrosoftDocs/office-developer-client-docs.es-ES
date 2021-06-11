---
title: IMAPIMessageSiteGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetLastError
api_type:
- COM
ms.assetid: 7ea282d7-388a-4f05-9780-f8dbc5c5d395
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: cc4de8aa21d4b3b27bf757389b663ebeff69a9cc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420741"
---
# <a name="imapimessagesitegetlasterror"></a>IMAPIMessageSite::GetLastError

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve una [estructura MAPIERROR](mapierror.md) que contiene información sobre el error anterior que se produjo en el objeto de sitio del mensaje. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parameters

 _hResult_
  
> [in] HRESULT que contiene el valor de error generado en la llamada al método anterior.
    
 _ulFlags_
  
> [in] Máscara de bits de marcas que controla el tipo de cadenas devueltas. Se puede establecer la siguiente marca:
    
MAPI_UNICODE 
  
> Las cadenas de la **estructura MAPIERROR** devueltas en el parámetro  _lppMAPIError_ están en formato Unicode. Si la MAPI_UNICODE no está establecida, las cadenas tienen el formato ANSI. 
    
 _lppMAPIError_
  
> [salida] Puntero a un puntero a la estructura **MAPIERROR** devuelta que contiene información de versión, componente y contexto del error. Este parámetro se puede establecer en NULL si no hay ninguna **estructura MAPIERROR** que devolver. 
    
## <a name="return-value"></a>Valor devuelto

S_OK
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_BAD_CHARWIDTH
  
> La marca MAPI_UNICODE se estableció y **GetLastError** no admite Unicode o MAPI_UNICODE no se estableció y **GetLastError** solo admite Unicode. 
    
## <a name="remarks"></a>Comentarios

El **método IMAPIMessageSite::GetLastError** proporciona información sobre una llamada al método anterior que ha fallado. Los autores de llamadas pueden proporcionar a sus usuarios información detallada sobre el error al incluir los datos de la estructura **MAPIERROR** en un cuadro de diálogo. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Puede usar la estructura **MAPIERROR** a la que apunta el parámetro  _lppMAPIError_ si MAPI proporciona uno solo si **GetLastError** devuelve S_OK. A veces MAPI no puede determinar cuál fue el último error o no tiene nada más que informar sobre el error. En esta situación, se devuelve un puntero a NULL en  _lppMAPIError_ en su lugar. 
  
Para obtener más información sobre el **método GetLastError,** vea [Using Extended Errors](mapi-extended-errors.md).
  
## <a name="see-also"></a>Vea también



[MAPIERROR](mapierror.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)

