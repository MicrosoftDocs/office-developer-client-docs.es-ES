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
# <a name="contab_entryid"></a>CONTAB_ENTRYID

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el identificador de entrada de la carpeta de contactos.
  
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
  
> Máscara de bits de marcas que proporciona información que describe el objeto. Para obtener más información, vea la descripción del **campo abFlags** de una [estructura ENTRYID.](entryid.md) 
    
 **muid**
  
> GUID que identifica el proveedor de almacén.
    
 **ulVersion**
  
> Número de versión de la **estructura CONTAB_ENTRYID** datos. Debe establecerse en CONTAB_VERSION. 
    
 **ulType**
  
> Entero que representa el tipo de identificador de entrada de contacto. Debe ser uno de los siguientes valores:
    
|**Nombre**|**Descripción**|
|:-----|:-----|
|CONTAB_USER  <br/> |Un objeto de usuario de mensajería.  <br/> |
|CONTAB_DISTLIST  <br/> |Un objeto de la lista de distribución.  <br/> |
   
 **ulIndex**
  
> Índice en el subconjunto de propiedades de correo electrónico.
    
 **cgnid**
  
> Tamaño del identificador de entrada del mensaje de contacto asociado a esta entrada en la Libreta de direcciones de contactos.
    
 **abeid**
  
> Identificador de entrada del mensaje de contacto asociado a esta entrada en la Libreta de direcciones de contactos.
    
## <a name="remarks"></a>Comentarios

Una libreta de direcciones de contactos es una libreta de direcciones que contiene todos los elementos de contacto de una carpeta contactos que tienen una dirección de correo electrónico o un número de fax. Cada entrada de una libreta de direcciones de contactos está asociada a una dirección de correo electrónico o a un número de fax. Dado que un elemento de contacto puede tener hasta tres direcciones de correo electrónico y tres números de fax, un elemento de contacto puede representarse mediante hasta seis entradas en la libreta de direcciones de contactos correspondiente.
  
El propósito de una libreta de direcciones de contactos es dar soporte a los usuarios que envían mensajes de correo electrónico a los contactos de una carpeta contactos. El proveedor de libreta de direcciones de contactos compatible con Microsoft Outlook 2010 y Microsoft Outlook 2013 contab32.dll.
  
La **CONTAB_ENTRYID** admite un subconjunto de la información que está presente en el mensaje de contacto MAPI subyacente. Identifica el mensaje de contacto al que está asociada una entrada de libreta de direcciones de contactos determinada. 
  
Los **campos ctipo y** **abeid** solo son válidos cuando el valor del campo **ulType** se establece en CONTAB_DISTLIST o CONTAB_USER. Cuando el valor del campo **ulType** se establece en CONTAB_ROOT, CONTAB_SUBROOT o [](dir_entryid.md) CONTAB_CONTAINER, se debe usar la estructura DIR_ENTRYID en su lugar. 
  
## <a name="see-also"></a>Consulte también



[DIR_ENTRYID](dir_entryid.md)


[Estructuras MAPI](mapi-structures.md)

