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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6b0a8923ee5efe22584170ce9853698885527ee8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407665"
---
# <a name="imapiprop--iunknown"></a>IMAPIProp : IUnknown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Permite que los clientes, proveedores de servicios y MAPI funcionen con propiedades. Todos los objetos que admiten propiedades implementan esta interfaz.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Expuesto por:  <br/> |Ningún objeto expone esta interfaz directamente.  <br/> |
|Implementado por:  <br/> |Proveedores de servicios y MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente, proveedores de servicios y MAPI  <br/> |
|Identificador de interfaz:  <br/> |IID_IMAPIProp  <br/> |
|Tipo de puntero:  <br/> |LPMAPIPROP  <br/> |
|Modelo de transacción:  <br/> |Clase abstracta, nunca implementada  <br/> |
   
## <a name="vtable-order"></a>Orden de tabla virtual

|||
|:-----|:-----|
|[GetLastError](imapiprop-getlasterror.md) <br/> |Devuelve una [estructura MAPIERROR](mapierror.md) que contiene información sobre el error anterior.  <br/> |
|[SaveChanges](imapiprop-savechanges.md) <br/> |Realiza de forma permanente los cambios realizados en un objeto desde la última operación de guardado.  <br/> |
|[GetProps](imapiprop-getprops.md) <br/> |Recupera el valor de propiedad de una o varias propiedades de un objeto.  <br/> |
|[GetPropList](imapiprop-getproplist.md) <br/> |Devuelve etiquetas de propiedad para todas las propiedades.  <br/> |
|[OpenProperty](imapiprop-openproperty.md) <br/> |Devuelve un puntero a una interfaz que se puede usar para tener acceso a una propiedad.  <br/> |
|[SetProps](imapiprop-setprops.md) <br/> |Actualiza una o más propiedades.  <br/> |
|[DeleteProps](imapiprop-deleteprops.md) <br/> |Elimina una o más propiedades de un objeto.  <br/> |
|[CopyTo](imapiprop-copyto.md) <br/> |Copia o mueve todas las propiedades, excepto las propiedades excluidas específicamente.  <br/> |
|[CopyProps](imapiprop-copyprops.md) <br/> |Copia o mueve las propiedades seleccionadas.  <br/> |
|[GetNamesFromIDs](imapiprop-getnamesfromids.md) <br/> |Proporciona los nombres de propiedad que corresponden a uno o más identificadores de propiedad.  <br/> |
|[GetIDsFromNames](imapiprop-getidsfromnames.md) <br/> |Proporciona los identificadores de propiedad que corresponden a uno o más nombres de propiedad.  <br/> |
   
## <a name="remarks"></a>Comentarios

 **IMAPIProp es** la interfaz base para las siguientes interfaces: 
  
- [IAttach](iattachimapiprop.md)
    
- [IMailUser](imailuserimapiprop.md)
    
- [IMAPIContainer](imapicontainerimapiprop.md)
    
- [IMAPIFormInfo](imapiforminfoimapiprop.md)
    
- [IMAPIStatus](imapistatusimapiprop.md)
    
- [IMessage](imessageimapiprop.md)
    
- [IMsgStore](imsgstoreimapiprop.md)
    
- [IProfSect](iprofsectimapiprop.md)
    
- [IPropData](ipropdataimapiprop.md)
    
## <a name="see-also"></a>Consulte también



[Interfaces MAPI](mapi-interfaces.md)

