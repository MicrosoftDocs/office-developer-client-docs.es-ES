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
ms.openlocfilehash: 2ef3bc973e12bd5630cc00b3c512b748d4a16e86
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409093"
---
# <a name="iattach--imapiprop"></a>IAttach : IMAPIProp

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Mantiene y proporciona acceso a las propiedades de los datos adjuntos de los mensajes. La **interfaz IAttach** no tiene métodos únicos propios. Para obtener más información acerca de cómo usar datos adjuntos, vea Datos adjuntos [mapi](mapi-attachments.md) y [tablas de datos adjuntos](attachment-tables.md). 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Expuesto por:  <br/> |Objetos de datos adjuntos  <br/> |
|Implementado por:  <br/> |Proveedores de al almacenamiento de mensajes  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente  <br/> |
|Identificador de interfaz:  <br/> |IID_IAttachment  <br/> |
|Tipo de puntero:  <br/> |LPATTACH  <br/> |
|Modelo de transacción:  <br/> |Transacted  <br/> |
   
## <a name="vtable-order"></a>Orden de tabla virtual

Esta interfaz no tiene ningún método único.
  
|**Propiedades requeridas**|**Access**|
|:-----|:-----|
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))  <br/> |Lectura/escritura  <br/> |
|**PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))  <br/> |Lectura/escritura  <br/> |
   
## <a name="see-also"></a>Consulte también



[Interfaces MAPI](mapi-interfaces.md)

