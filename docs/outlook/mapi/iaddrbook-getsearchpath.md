---
title: IAddrBookGetSearchPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.GetSearchPath
api_type:
- COM
ms.assetid: 43b51a66-71fa-4e10-93e4-d533b48af4de
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: f8c129e772870804ef464765b2035a3582317a09
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412985"
---
# <a name="iaddrbookgetsearchpath"></a>IAddrBook::GetSearchPath

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve una lista ordenada de identificadores de entrada de los contenedores que se incluirán en el proceso de resolución de nombres Iniciado por el método [IAddrBook:: ResolveName](iaddrbook-resolvename.md) . 
  
```cpp
HRESULT GetSearchPath(
  ULONG ulFlags,
  LPSRowSet FAR * lppSearchPath
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> a Máscara de máscara de marcadores que controla el tipo de las cadenas devueltas en la ruta de búsqueda. Se puede establecer la siguiente marca:
    
MAPI_UNICODE 
  
> Las cadenas devueltas están en formato Unicode. Si no se establece la marca MAPI_UNICODE, las cadenas están en formato ANSI.
    
 _lppSearchPath_
  
> contempla Un puntero a un puntero a una lista ordenada de identificadores de entrada de contenedor. **GetSearchPath** almacena la lista ordenada en una estructura [SRowSet](srowset.md) . Si no hay ningún contenedor en la jerarquía de la libreta de direcciones, se devuelve cero en la estructura **SRowSet** . 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La ruta de búsqueda se recuperó correctamente.
    
## <a name="remarks"></a>Comentarios

Los clientes y los proveedores de servicios llaman al método **GetSearchPath** para obtener la ruta de búsqueda que se usa para resolver los nombres con el método **ResolveName** . Normalmente, los clientes llaman al método [IAddrBook:: SetSearchPath](iaddrbook-setsearchpath.md) para establecer una ruta de búsqueda de contenedor en el perfil antes de llamar a **GetSearchPath** para recuperarlo. Sin embargo, llamar a **SetSearchPath** es opcional. 
  
Si nunca se ha llamado a **SetSearchPath** , **GetSearchPath** crea una ruta de acceso al trabajar con las tablas de jerarquía de la libreta de direcciones. La ruta de búsqueda predeterminada establecida por **GetSearchPath** consta de los siguientes contenedores en el orden siguiente: 
  
1. El primer contenedor con permiso de lectura y escritura, normalmente la libreta personal de direcciones (PAB).
    
2. Cada contenedor que tiene su propiedad **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) establecida en DT_GLOBAL. Este valor indica que el contenedor contiene los destinatarios. 
    
3. El contenedor designado como predeterminado, si no hay contenedores que tienen la marca DT_GLOBAL establecida en su propiedad **PR_DISPLAY_TYPE** y el contenedor predeterminado difiere del primer contenedor con permiso de lectura y escritura. 
    
Si se ha llamado a **SetSearchPath** , **GetSearchPath** crea una ruta de acceso mediante los contenedores de la libreta de direcciones que se han almacenado en el perfil. **GetSearchPath** valida esta ruta antes de que la devuelva al autor de la llamada. 
  
Después de la primera llamada a **SetSearchPath**, se deben usar las llamadas posteriores a **SetSearchPath** para modificar la ruta de búsqueda devuelta por **GetSearchPath**. Es decir, el proveedor o el cliente que realiza la llamada no recibe la ruta de búsqueda predeterminada después de la primera llamada a **SetSearchPath**.
  
## <a name="see-also"></a>Ver también



[IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md)
  
[SRowSet](srowset.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

