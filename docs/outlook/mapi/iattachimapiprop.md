---
title: IAttach IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAttach
api_type:
- COM
ms.assetid: f47e20e1-2a30-4c9e-8ca6-e8c5e72f44a1
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 66e318c3b7b772f2713b5c730590ce4a8ad5965b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817141"
---
# <a name="iattach--imapiprop"></a>IAttach : IMAPIProp

  
  
**Hace referencia a**: Outlook 
  
Mantiene y proporciona acceso a las propiedades de los datos adjuntos en los mensajes. La interfaz **IAttach** no tiene únicos métodos de su propio. Para obtener más información acerca de cómo usar los datos adjuntos, vea [Los datos adjuntos de MAPI](mapi-attachments.md) y [Las tablas de datos adjuntos](attachment-tables.md). 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Expuestos por:  <br/> |Objetos de datos adjuntos  <br/> |
|Se implementa mediante:  <br/> |Proveedores de almacén de mensajes  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente  <br/> |
|Identificador de interfaz:  <br/> |IID_IAttachment  <br/> |
|Tipo de puntero:  <br/> |LPATTACH  <br/> |
|Modelo de transacciones:  <br/> |Negocian  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

Esta interfaz no tiene ningún método único.
  
|**Propiedades requeridas**|**Access**|
|:-----|:-----|
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))  <br/> |Es de lectura y escritura.  <br/> |
|**PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))  <br/> |Es de lectura y escritura.  <br/> |
   
## <a name="see-also"></a>Vea también



[Interfaces MAPI](mapi-interfaces.md)

