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
ms.openlocfilehash: ff088dc5bf62f407692c9eec649ff388f79d549d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567156"
---
# <a name="contabentryid"></a>CONTAB_ENTRYID

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Contiene el identificador de entrada de la carpeta Contactos.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |msomapiutil.h  <br/> |
   
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

## <a name="members"></a>Miembros

 **abFlags**
  
> Una máscara de bits de indicadores que proporciona información que describe el objeto. Para obtener más información, vea la descripción del campo **abFlags** de una estructura de [ENTRYID](entryid.md) . 
    
 **muid**
  
> GUID que identifica el proveedor de almacenamiento.
    
 **ulVersion**
  
> El número de versión de la estructura **CONTAB_ENTRYID** . Debe establecerse en CONTAB_VERSION. 
    
 **ulType**
  
> Un entero que representa el tipo de identificador de entrada del contacto. Debe ser uno de los siguientes valores:
    
|**Nombre**|**Descripción**|
|:-----|:-----|
|CONTAB_USER  <br/> |Un objeto de usuario de mensajería.  <br/> |
|CONTAB_DISTLIST  <br/> |Un objeto de la lista de distribución.  <br/> |
   
 **ulIndex**
  
> El índice en el subconjunto de la propiedad de correo electrónico.
    
 **cbeid**
  
> El tamaño del identificador de entrada del mensaje contacto asociado con esta entrada de la libreta de direcciones de contactos.
    
 **abeid**
  
> El identificador de entrada del mensaje contacto asociado con esta entrada de la libreta de direcciones de contactos.
    
## <a name="remarks"></a>Comentarios

Una libreta de direcciones de contactos es una libreta de direcciones que contiene todos los elementos de contacto en una carpeta de contactos que tienen una dirección de correo electrónico o un número de fax. Cada entrada de una libreta de direcciones de contactos está asociado con una dirección de correo electrónico o un número de fax. Dado que un elemento de contacto puede tener hasta tres direcciones de correo electrónico y tres números de fax, se puede representar un elemento de contacto por hasta seis entradas en la libreta de direcciones de los contactos correspondientes.
  
El propósito de una libreta de direcciones de contactos es admitir los usuarios hacer frente a los mensajes de correo electrónico a los contactos en una carpeta de contactos. El proveedor de la libreta de direcciones de contactos compatibles con Microsoft Outlook 2010 y Microsoft Outlook 2013 es contab32.dll.
  
La estructura **CONTAB_ENTRYID** admite un subconjunto de la información que está presente en el mensaje de contacto de MAPI subyacente. Identifica el mensaje de contacto que está asociada una entrada de la libreta de direcciones de contactos determinada. 
  
Los campos **cbeid** y **abeid** sólo son válidos cuando se establece el valor del campo **ulType** en CONTAB_DISTLIST o CONTAB_USER. Cuando se establece el valor del campo **ulType** en CONTAB_ROOT, CONTAB_SUBROOT o CONTAB_CONTAINER, la estructura [DIR_ENTRYID](dir_entryid.md) debe usarse en su lugar. 
  
## <a name="see-also"></a>Vea también



[DIR_ENTRYID](dir_entryid.md)


[Estructuras MAPI](mapi-structures.md)

