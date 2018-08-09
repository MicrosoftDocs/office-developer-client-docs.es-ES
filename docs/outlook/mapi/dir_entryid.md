---
title: DIR_ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9e055269-f3bf-4b64-8384-3cbc372c0b34
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 2af9d529cb92e1040427eba69270908dcf4a5d9f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816688"
---
# <a name="direntryid"></a>DIR_ENTRYID

  
  
**Hace referencia a**: Outlook 
  
Se describen las propiedades de un identificador de entrada de Active directory.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |EntryID.h  <br/> |
   
```cpp
#pragma pack(4)
typedef struct _dir_entryid
{
    BYTE abFlags[4]; 
    MAPIUID muid; 
    ULONG ulVersion; 
    ULONG ulType; 
    MAPIUID muidID; 
}   DIR_ENTRYID, *LPDIR_ENTRYID; 
#pragma pack()
```

## <a name="members"></a>Members

 **abFlags**
  
> Una máscara de bits de indicadores que proporciona información que describe el objeto. Para obtener más información, vea la descripción del campo **abFlags** de una estructura de [ENTRYID](entryid.md) . 
    
 **muid**
  
> GUID que identifica el proveedor de almacenamiento.
    
 **ulVersion**
  
> El número de versión de la estructura **DIR_ENTRYID** . Debe establecerse en CONTAB_VERSION. 
    
 **ulType**
  
> Un entero que representa el tipo de identificador de entrada de Active directory. Debe ser uno de los siguientes valores:
    
|**Nombre**|**Descripción**|
|:-----|:-----|
|CONTAB_ROOT  <br/> |La carpeta raíz de una libreta de direcciones MAPI.  <br/> |
|CONTAB_SUBROOT  <br/> |Una subcarpeta dentro de la carpeta raíz del objeto de la libreta de direcciones MAPI.  <br/> |
|CONTAB_CONTAINER  <br/> |Un objeto de contenedor de libreta de direcciones.  <br/> |
   
 **muidID**
  
> Un GUID que identifica el objeto de inicio de sesión.
    
## <a name="remarks"></a>Comentarios

Las estructuras de **DIR_ENTRYID** y [CONTAB_ENTRYID](contab_entryid.md) son idénticas, excepto por el miembro **ulType** . El contenido del miembro **ulType** determina qué estructura es apropiada para los campos restantes. 
  
## <a name="see-also"></a>Vea también



[CONTAB_ENTRYID](contab_entryid.md)


[Estructuras MAPI](mapi-structures.md)

