---
title: Propiedad canónica PidTagWizardNoPstPage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagWizardNoPstPage
api_type:
- COM
ms.assetid: 1ac09578-892b-4c72-92f6-c2419ac2efe8
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e816af2ce60b4c06ae14f720cf7c36d58468d09d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422890"
---
# <a name="pidtagwizardnopstpage-canonical-property"></a>Propiedad canónica PidTagWizardNoPstPage

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Esta propiedad contiene TRUE si el asistente para perfiles va a suprimir la página de almacén de mensajes personales (PST).
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_WIZARD_NO_PST_PAGE  <br/> |
|Identificador:  <br/> |0x6700  <br/> |
|Tipo de datos:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Exchange Administrativo  <br/> |
   
## <a name="remarks"></a>Comentarios

Los proveedores de servicios pueden establecer esta propiedad al llamar a una función basada en el prototipo de [función LAUNCHWIZARDENTRY.](launchwizardentry.md) Esta propiedad indica al asistente de perfil que el proveedor no desea que se muestre la página PST durante el cuadro de diálogo del usuario. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como propiedades asociadas.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

