---
title: IProviderAdminGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin.GetLastError
api_type:
- COM
ms.assetid: 853ddee5-24d6-423d-b483-6a07a12de51f
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 4fc4867d5ca20f8e770afa239b0dffbd8ab1c480
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439852"
---
# <a name="iprovideradmingetlasterror"></a>IProviderAdmin::GetLastError

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el error anterior que se produjo en el objeto de administración del proveedor. 
  
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
  
> a Máscara de máscara de marcadores que controla el tipo de cadenas devueltas. Se puede establecer la siguiente marca:
    
MAPI_UNICODE 
  
> Las cadenas de **MAPIERROR** devueltas en el parámetro _lppMAPIError_ están en formato Unicode. Si no se establece la marca MAPI_UNICODE, las cadenas están en formato ANSI. 
    
 _lppMAPIError_
  
> contempla Un puntero a un puntero a la estructura **MAPIERROR** devuelta que contiene la información de versión, componente y contexto del error. El parámetro _lppMAPIError_ puede establecerse en NULL si no hay ningún **MAPIERROR** para devolver. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y ha devuelto el valor o los valores esperados.
    
MAPI_E_BAD_CHARWIDTH 
  
> Se estableció la marca MAPI_UNICODE y **GetLastError** no admite Unicode, o bien no se estableció MAPI_UNICODE y **GetLastError** solo admite Unicode. 
    
## <a name="remarks"></a>Comentarios

El método **IProviderAdmin:: GetLastError** proporciona información sobre una llamada a un método anterior que produjo un error. Los autores de llamadas pueden proporcionar a sus usuarios información detallada acerca del error al incluir los datos de la estructura **MAPIERROR** en un cuadro de diálogo. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Puede usar la estructura **MAPIERROR** , si MAPI proporciona una, a la que apunta el parámetro _LppMAPIError_ solo si **GetLastError** Devuelve S_OK. A veces MAPI no puede determinar el último error o no tiene nada más para informar sobre el error. En esta situación, un puntero a NULL se devuelve en _lppMAPIError_ en su lugar. 
  
Para obtener más información sobre el método **GetLastError** , consulte [Using Extended Errors](mapi-extended-errors.md).
  
## <a name="see-also"></a>Ver también



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IProviderAdmin : IUnknown](iprovideradminiunknown.md)

