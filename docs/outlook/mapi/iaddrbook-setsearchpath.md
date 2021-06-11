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
ms.openlocfilehash: 8611249207811446ae47f056486ec498bf1e7eab
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426208"
---
# <a name="iaddrbooksetsearchpath"></a>IAddrBook::SetSearchPath

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Establece una nueva ruta de búsqueda en el perfil que se usa para el proceso de resolución de nombres. 
  
```cpp
HRESULT SetSearchPath(
  ULONG ulFlags,
  LPSRowSet lpSearchPath
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
 _lpSearchPath_
  
> [in] Puntero a la [estructura SRowSet](srowset.md) usada para contener la ruta de búsqueda. La primera propiedad para cada **miembro de aRow** en **SRowSet** debe ser **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La ruta de búsqueda se estableció correctamente.
    
MAPI_E_MISSING_REQUIRED_COLUMN 
  
> Uno de los contenedores descritos en la **estructura SRowSet** no incluye su **PR_ENTRYID** propiedad. 
    
## <a name="remarks"></a>Comentarios

Los clientes y proveedores de servicios llaman al **método SetSearchPath** para guardar los cambios realizados en el orden de búsqueda del contenedor que se usa para resolver nombres con el método [IAddrBook::ResolveName.](iaddrbook-resolvename.md) La ruta de búsqueda se guarda entre instancias de una sesión. 
  
Los clientes y proveedores no tienen que llamar al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) para que la ruta de búsqueda cambie de forma permanente. 
  
## <a name="see-also"></a>Vea también



[IAddrBook::GetDefaultDir](iaddrbook-getdefaultdir.md)
  
[IAddrBook::GetPAB](iaddrbook-getpab.md)
  
[IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md)
  
[Propiedad canónica PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

