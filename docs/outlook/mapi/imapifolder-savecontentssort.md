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
ms.openlocfilehash: c142424bb050ae287f54a87ea8a5e0ea45acb12c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351208"
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

## <a name="parameters"></a>Parameters

 _lpSortCriteria_
  
> a Un puntero a una estructura [SSortOrderSet](ssortorderset.md) que contiene el criterio de ordenación predeterminado. 
    
 _ulFlags_
  
> a Máscara de máscara de marcadores que controla cómo se establece el criterio de ordenación predeterminado. Se puede establecer la siguiente marca:
    
RECURSIVE_SORT 
  
> El valor predeterminado de criterio de ordenación se aplica a la carpeta indicada y a todas sus subcarpetas.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El criterio de ordenación se guardó correctamente.
    
MAPI_E_NO_SUPPORT 
  
> El proveedor de almacenamiento de mensajes no admite guardar un criterio de ordenación para las tablas de contenido de la carpeta.
    
## <a name="remarks"></a>Comentarios

El método **IMAPIFolder:: SaveContentsSort** establece un criterio de ordenación predeterminado para la tabla de contenido de una carpeta. Es decir, cuando un cliente llama al método [IMAPIContainer:: GetContentsTable](imapicontainer-getcontentstable.md) de la carpeta después de que el código llama a **SaveContentsSort**, las filas de la tabla contenido devuelto aparecerán en el orden establecido por **SaveContentsSort**.
  
No todos los proveedores de almacenamiento de mensajes admiten **SaveContentsSort**; es aceptable para los proveedores de almacenamiento de mensajes devolver MAPI_E_NO_SUPPORT desde el método **SaveContentsSort** . 
  
## <a name="see-also"></a>Vea también



[IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)
  
[SSortOrderSet](ssortorderset.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)

