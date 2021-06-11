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
ms.openlocfilehash: e7abcb2c86ff5cabe0b8f5664ec316244617ac09
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421238"
---
# <a name="dir_entryid"></a>DIR_ENTRYID

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Describe las propiedades de un identificador de entrada de directorio.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |entryid.h  <br/> |
   
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
  
> Máscara de bits de marcas que proporciona información que describe el objeto. Para obtener más información, vea la descripción del **campo abFlags** de una [estructura ENTRYID.](entryid.md) 
    
 **muid**
  
> GUID que identifica el proveedor de almacenamiento.
    
 **ulVersion**
  
> Número de versión de la **DIR_ENTRYID** estructura. Debe establecerse en CONTAB_VERSION. 
    
 **ulType**
  
> Entero que representa el tipo de identificador de entrada de directorio. Debe ser uno de los siguientes valores:
    
|**Nombre**|**Descripción**|
|:-----|:-----|
|CONTAB_ROOT  <br/> |Carpeta raíz de una libreta de direcciones MAPI.  <br/> |
|CONTAB_SUBROOT  <br/> |Una subcarpeta incluida en la carpeta raíz del objeto de la libreta de direcciones MAPI.  <br/> |
|CONTAB_CONTAINER  <br/> |Un objeto contenedor de libreta de direcciones.  <br/> |
   
 **muidID**
  
> GUID que identifica el objeto de inicio de sesión.
    
## <a name="remarks"></a>Comentarios

Las estructuras **DIR_ENTRYID** y [CONTAB_ENTRYID](contab_entryid.md) son idénticas, excepto para el **miembro ulType.** El contenido del miembro **ulType** determina qué estructura es adecuada para los campos restantes. 
  
## <a name="see-also"></a>Vea también



[CONTAB_ENTRYID](contab_entryid.md)


[Estructuras MAPI](mapi-structures.md)

