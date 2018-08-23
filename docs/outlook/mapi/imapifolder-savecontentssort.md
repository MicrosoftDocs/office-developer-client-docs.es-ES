---
title: IMAPIFolderSaveContentsSort
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.SaveContentsSort
api_type:
- COM
ms.assetid: 5ae3fdf0-6193-4c1f-bd2e-d69c56d69773
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 1f79265c4356747e64aa8102dd4486db229baf5a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579665"
---
# <a name="imapifoldersavecontentssort"></a>IMAPIFolder::SaveContentsSort

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Establece el criterio de ordenación predeterminado para la tabla de contenido de una carpeta.
  
```cpp
HRESULT SaveContentsSort(
  LPSSortOrderSet lpSortCriteria,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parámetros

 _lpSortCriteria_
  
> [entrada] Un puntero a una estructura [SSortOrderSet](ssortorderset.md) que contiene el criterio de ordenación predeterminado. 
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla cómo se establece el criterio de ordenación predeterminado. Se puede establecer la marca siguiente:
    
RECURSIVE_SORT 
  
> El conjunto de criterio de ordenación predeterminado se aplica a la carpeta indicada y a todas sus subcarpetas.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El criterio de ordenación se guardó correctamente.
    
MAPI_E_NO_SUPPORT 
  
> El proveedor de almacén de mensajes no admite guardar un criterio de ordenación para sus tablas de contenido de carpeta.
    
## <a name="remarks"></a>Comentarios

El método **IMAPIFolder::SaveContentsSort** establece un criterio de ordenación predeterminado para la tabla de contenido de una carpeta. Es decir, cuando un cliente llama (método) [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) de la carpeta después de las llamadas de código **SaveContentsSort**, las filas de la tabla de contenido devuelto se muestra en el orden establecido por **SaveContentsSort**.
  
No todos los proveedores de almacén de mensajes admiten **SaveContentsSort**; es aceptable para los proveedores de almacén de mensajes devolver MAPI_E_NO_SUPPORT desde el método **SaveContentsSort** . 
  
## <a name="see-also"></a>Recursos adicionales



[IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)
  
[SSortOrderSet](ssortorderset.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)

