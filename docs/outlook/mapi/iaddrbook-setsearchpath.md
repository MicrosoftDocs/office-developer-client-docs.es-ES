---
title: IAddrBookSetSearchPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.SetSearchPath
api_type:
- COM
ms.assetid: fbff82de-77d3-411e-a30c-a37cefdd92fc
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 1d486344ab20ef49488dbb911f3dd7000d64942e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571762"
---
# <a name="iaddrbooksetsearchpath"></a>IAddrBook::SetSearchPath

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Establece una nueva ruta de acceso de búsqueda en el perfil que se usa para el proceso de resolución de nombres. 
  
```cpp
HRESULT SetSearchPath(
  ULONG ulFlags,
  LPSRowSet lpSearchPath
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
 _lpSearchPath_
  
> [entrada] Un puntero a la estructura [SRowSet](srowset.md) que se utiliza para contener la ruta de acceso de búsqueda. La primera propiedad para cada miembro de **aRow** de **SRowSet** debe ser una **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)).
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La ruta de acceso de búsqueda se estableció correctamente.
    
MAPI_E_MISSING_REQUIRED_COLUMN 
  
> Uno de los contenedores que se describen en la estructura **SRowSet** no incluía su propiedad de **entrada del objeto** . 
    
## <a name="remarks"></a>Comentarios

Los clientes y proveedores de servicios de llamar al método **SetSearchPath** para guardar los cambios realizados en el orden de búsqueda de contenedor que se utiliza para resolver nombres con el método [IAddrBook::ResolveName](iaddrbook-resolvename.md) . Se guarda la ruta de acceso de búsqueda entre instancias de una sesión. 
  
Los clientes y proveedores no es necesario que llamar al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) para que los cambios de la ruta de acceso de búsqueda sea permanente. 
  
## <a name="see-also"></a>Recursos adicionales



[IAddrBook::GetDefaultDir](iaddrbook-getdefaultdir.md)
  
[IAddrBook::GetPAB](iaddrbook-getpab.md)
  
[IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md)
  
[Propiedad canónica PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

