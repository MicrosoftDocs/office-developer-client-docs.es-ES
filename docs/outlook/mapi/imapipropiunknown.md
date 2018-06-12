---
title: IMAPIProp IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp
api_type:
- COM
ms.assetid: 3c9e4e05-cd3a-4b56-9dff-879e33ff6fd5
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 02d2b136ed1437ba53ce1e54a202d70a48b2abe9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817427"
---
# <a name="imapiprop--iunknown"></a>IMAPIProp: IUnknown

  
  
**Se aplica a**: Outlook 
  
Permite a los clientes, proveedores de servicios y MAPI trabajar con propiedades. Todos los objetos que admiten propiedades implementar esta interfaz.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Expuestos por:  <br/> |No hay ningún objeto expone esta interfaz directamente.  <br/> |
|Se implementa mediante:  <br/> |Proveedores de servicios y MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente, los proveedores de servicios y MAPI  <br/> |
|Identificador de interfaz:  <br/> |IID_IMAPIProp  <br/> |
|Tipo de puntero:  <br/> |LPMAPIPROP  <br/> |
|Modelo de transacciones:  <br/> |Clase abstracta, que nunca se ha implementado  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[GetLastError](imapiprop-getlasterror.md) <br/> |Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el error anterior.  <br/> |
|[SaveChanges](imapiprop-savechanges.md) <br/> |Hace permanentes los cambios realizados a un objeto desde la última operación de guardar.  <br/> |
|[GetProps](imapiprop-getprops.md) <br/> |Recupera el valor de la propiedad de una o varias propiedades de un objeto.  <br/> |
|[GetPropList](imapiprop-getproplist.md) <br/> |Devuelve las etiquetas de propiedad para todas las propiedades.  <br/> |
|[OpenProperty](imapiprop-openproperty.md) <br/> |Devuelve un puntero a una interfaz que se puede usar para obtener acceso a una propiedad.  <br/> |
|[SetProps](imapiprop-setprops.md) <br/> |Actualiza las propiedades de uno o más.  <br/> |
|[DeleteProps](imapiprop-deleteprops.md) <br/> |Elimina una o más propiedades de un objeto.  <br/> |
|[CopyTo](imapiprop-copyto.md) <br/> |Copia o mueve todas las propiedades, excepto propiedades excluidas específicamente.  <br/> |
|[CopyProps](imapiprop-copyprops.md) <br/> |Copia o mueve las propiedades seleccionadas.  <br/> |
|[GetNamesFromIDs](imapiprop-getnamesfromids.md) <br/> |Proporciona los nombres de propiedad que se corresponden con uno o varios identificadores de propiedad.  <br/> |
|[A GetIDsFromNames](imapiprop-getidsfromnames.md) <br/> |Proporciona los identificadores de propiedad que se corresponden con uno o varios nombres de propiedad.  <br/> |
   
## <a name="remarks"></a>Notas

 **IMAPIProp** es la interfaz base para las interfaces siguientes: 
  
- [IAttach](iattachimapiprop.md)
    
- [IMailUser](imailuserimapiprop.md)
    
- [IMAPIContainer](imapicontainerimapiprop.md)
    
- [IMAPIFormInfo](imapiforminfoimapiprop.md)
    
- [IMAPIStatus](imapistatusimapiprop.md)
    
- [IMessage](imessageimapiprop.md)
    
- [IMsgStore](imsgstoreimapiprop.md)
    
- [IProfSect](iprofsectimapiprop.md)
    
- [IPropData](ipropdataimapiprop.md)
    
## <a name="see-also"></a>Ver también



[Interfaces MAPI](mapi-interfaces.md)

