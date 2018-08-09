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
ms.openlocfilehash: b94e1f2d66f89d680cc738968342de0fbcee5cda
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/15/2018
ms.locfileid: "19820424"
---
# <a name="pidtagwizardnopstpage-canonical-property"></a>Propiedad canónica PidTagWizardNoPstPage

  
  
**Hace referencia a**: Outlook 
  
Esta propiedad contiene TRUE si el Asistente de perfil suprimir la página de almacén (PST) de mensaje personal.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_WIZARD_NO_PST_PAGE  <br/> |
|Identificador:  <br/> |0x6700  <br/> |
|Tipo de datos:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Exchange, administrativo  <br/> |
   
## <a name="remarks"></a>Comentarios

Proveedores de servicios pueden establecer esta propiedad cuando se llama a una función según el prototipo de función [LAUNCHWIZARDENTRY](launchwizardentry.md) . Esta propiedad indica al Asistente para perfiles que el proveedor no desea que se muestre durante el cuadro de diálogo de usuario en la página de PST. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de propiedades que se muestran como propiedades asociadas.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

