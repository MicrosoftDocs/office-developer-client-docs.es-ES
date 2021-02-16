---
title: IMAPIFormContainerGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.GetLastError
api_type:
- COM
ms.assetid: 04952b51-f005-4933-a1d1-695c6dc736cc
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: e020c66a46f1f195a5731ef1cb3f4b0488162a2b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415673"
---
# <a name="imapiformcontainergetlasterror"></a>IMAPIFormContainer::GetLastError

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve una [estructura MAPIERROR](mapierror.md) que contiene información sobre el error anterior generado por el objeto contenedor de formulario. 
  
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
  
> Las cadenas de la [estructura MAPIERROR](mapierror.md) devueltas en el parámetro  _lppMAPIError_ están en formato Unicode. Si no MAPI_UNICODE marca, las cadenas están en formato ANSI. 
    
 _lppMAPIError_
  
> [salida] Puntero a un puntero a la estructura **MAPIERROR** devuelta que contiene información de versión, componente y contexto del error. El  _parámetro lppMAPIError_ se puede establecer en NULL si no hay ninguna **estructura MAPIERROR** que devolver. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_BAD_CHARWIDTH 
  
> Se estableció MAPI_UNICODE marca y **GetLastError** no admite Unicode o MAPI_UNICODE no se estableció **y GetLastError** solo admite Unicode. 
    
## <a name="remarks"></a>Comentarios

El **método IMAPIFormContainer::GetLastError** proporciona información sobre una llamada de método anterior que ha fallado. Los autores de llamadas pueden proporcionar a sus usuarios información detallada sobre el error incluyendo los datos de la estructura **MAPIERROR** en un cuadro de diálogo. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Puede usar la estructura **MAPIERROR** a la que apunta el parámetro  _lppMAPIError_ si MAPI proporciona una solo si **GetLastError** devuelve S_OK. A veces MAPI no puede determinar cuál fue el último error o no tiene nada más que informar sobre el error. En esta situación, se devuelve un puntero a NULL  _en lppMAPIError_ en su lugar. 
  
Para obtener más información acerca **del método GetLastError,** vea [El uso de errores extendidos.](mapi-extended-errors.md)
  
## <a name="see-also"></a>Consulte también



[MAPIERROR](mapierror.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)

