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
ms.openlocfilehash: 7bf69e560142ab282d6545389e02766389e4d018
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580701"
---
# <a name="iaddrbookgetsearchpath"></a>IAddrBook::GetSearchPath

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve una lista ordenada de los identificadores de entrada de los contenedores que se deben incluir en el proceso de resolución de nombres iniciado por el método [IAddrBook::ResolveName](iaddrbook-resolvename.md) . 
  
```cpp
HRESULT GetSearchPath(
  ULONG ulFlags,
  LPSRowSet FAR * lppSearchPath
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla el tipo de las cadenas devueltas en la ruta de acceso de búsqueda. Se puede establecer la marca siguiente:
    
MAPI_UNICODE. 
  
> Las cadenas devueltas están en formato Unicode. Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI.
    
 _lppSearchPath_
  
> [out] Un puntero a un puntero a una lista ordenada de identificadores de entrada del contenedor. **GetSearchPath** almacena la lista ordenada en una estructura [SRowSet](srowset.md) . Si no hay ningún contenedores en la jerarquía de la libreta de direcciones, se devuelve cero en la estructura **SRowSet** . 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La ruta de acceso de búsqueda se recuperó correctamente.
    
## <a name="remarks"></a>Comentarios

Los clientes y proveedores de servicios de llamar al método **GetSearchPath** para obtener la ruta de acceso de búsqueda que se utiliza para resolver nombres con el método **ResolveName** . Normalmente, los clientes de llaman al método [IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md) para establecer una ruta de acceso de búsqueda de contenedor en el perfil antes de llamar a **GetSearchPath** para recuperarlo. Sin embargo, al llamar a **SetSearchPath** es opcional. 
  
Si nunca se ha llamado **SetSearchPath** , **GetSearchPath** genera una ruta de acceso por trabajar a través de la dirección de las tablas de jerarquía del libro. La ruta de acceso de búsqueda predeterminada establecida por **GetSearchPath** consta de los siguientes contenedores en el orden siguiente: 
  
1. El primer contenedor con permiso de lectura y escritura, generalmente la libreta de direcciones personales (PAB).
    
2. Cada contenedor que tenga su propiedad **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) que se establece en DT_GLOBAL. Esta configuración indica que el contenedor contiene a los destinatarios. 
    
3. El contenedor designado como el valor predeterminado, si no hay ningún contenedores que tienen la marca DT_GLOBAL establecer en su propiedad **PR_DISPLAY_TYPE** y el contenedor predeterminado difiere del primer contenedor con permiso de lectura y escritura. 
    
Si se ha llamado **SetSearchPath** , **GetSearchPath** crea una ruta de acceso mediante el uso de los contenedores de la libreta de direcciones que se han almacenado en el perfil. **GetSearchPath** valida esta ruta de acceso antes de lo devuelve al autor de la llamada. 
  
Después de la primera llamada a **SetSearchPath**, las llamadas subsiguientes a **SetSearchPath** se deben usar para modificar la ruta de acceso de búsqueda devuelto por **GetSearchPath**. En otras palabras, el cliente o el proveedor realiza la llamada no recibe la ruta de acceso de búsqueda predeterminada después de la primera llamada a **SetSearchPath**.
  
## <a name="see-also"></a>Recursos adicionales



[IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md)
  
[SRowSet](srowset.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

