---
title: CONTAB_ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 84251222-dac4-4f4d-97b9-aa0e2cd26c44
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a2a204f76b62c8c6bc6d8a4e793c936a0184dc65
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424087"
---
# <a name="contabentryid"></a>CONTAB_ENTRYID

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el identificador de entrada de la carpeta de contactos.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |msomapiutil. h  <br/> |
   
```cpp
#pragma pack(4) 
typedef struct _contab_entryid
{
    BYTE abFlags[4];
    MAPIUID muid;
    ULONG ulVersion;
    ULONG ulType;
    ULONG ulIndex;
    ULONG cbeid;
    BYTE abeid[1];
}   CONTAB_ENTRYID, *LPCONTAB_ENTRYID;
#pragma pack() 
```

## <a name="members"></a>Members

 **abFlags**
  
> Máscara de máscara de marcadores que proporciona información que describe el objeto. Para obtener más información, vea la descripción del campo **abFlags** de una estructura [EntryID](entryid.md) . 
    
 **Muid**
  
> GUID que identifica el proveedor de almacenamiento.
    
 **ulVersion**
  
> Número de versión de la estructura **CONTAB_ENTRYID** . Debe establecerse en CONTAB_VERSION. 
    
 **ulType**
  
> Entero que representa el tipo de identificador de la entrada de contacto. Debe ser uno de los siguientes valores:
    
|**Nombre**|**Descripción**|
|:-----|:-----|
|CONTAB_USER  <br/> |Un objeto de usuario de mensajería.  <br/> |
|CONTAB_DISTLIST  <br/> |Un objeto de la lista de distribución.  <br/> |
   
 **ulIndex**
  
> Índice en el subconjunto de propiedades de correo electrónico.
    
 **cbeid**
  
> El tamaño del identificador de entrada del mensaje de contacto asociado con esta entrada en la libreta de direcciones de contactos.
    
 **Abeid**
  
> Identificador de entrada del mensaje de contacto asociado con esta entrada en la libreta de direcciones de contactos.
    
## <a name="remarks"></a>Comentarios

Una libreta de direcciones de contactos es una libreta de direcciones que contiene todos los elementos de contacto de una carpeta de contactos que tienen una dirección de correo electrónico o un número de fax. Cada entrada de una libreta de direcciones de contactos está asociada con una dirección de correo electrónico o un número de fax. Dado que un elemento de contacto puede tener hasta tres direcciones de correo electrónico y tres números de fax, un elemento de contacto puede representarse en un máximo de seis entradas en la libreta de direcciones de contactos correspondiente.
  
La finalidad de una libreta de direcciones de contactos es admitir que los usuarios que dirigen mensajes de correo electrónico a los contactos de una carpeta de contactos. El proveedor de la libreta de direcciones de contactos que admite Microsoft Outlook 2010 y Microsoft Outlook 2013 es contab32. dll.
  
La estructura **CONTAB_ENTRYID** admite un subconjunto de la información que se encuentra en el mensaje de contacto de MAPI subyacente. Identifica el mensaje de contacto al que está asociada una entrada específica de la libreta de direcciones de contactos. 
  
Los campos **cbeid** y **Abeid** solo son válidos cuando el valor del campo **ulType** está establecido en CONTAB_DISTLIST o CONTAB_USER. Cuando el valor del campo **ulType** se establece en CONTAB_ROOT, CONTAB_SUBROOT o CONTAB_CONTAINER, se debe usar la estructura [DIR_ENTRYID](dir_entryid.md) en su lugar. 
  
## <a name="see-also"></a>Ver también



[DIR_ENTRYID](dir_entryid.md)


[Estructuras MAPI](mapi-structures.md)

