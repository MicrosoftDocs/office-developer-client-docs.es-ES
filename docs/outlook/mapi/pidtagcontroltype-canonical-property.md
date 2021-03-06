---
title: Propiedad canónica PidTagControlType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagControlType
api_type:
- HeaderDef
ms.assetid: 7728fa2f-4a59-4e86-90f1-4384824598aa
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7bdb02f72ba14a36c8a4c218cd5f0631e7145e6a
ms.sourcegitcommit: 0419850d5c1b3439d9da59070201fb4952ca5d07
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/28/2020
ms.locfileid: "49734206"
---
# <a name="pidtagcontroltype-canonical-property"></a>Propiedad canónica PidTagControlType

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene un valor que indica un tipo de control para un control usado en un cuadro de diálogo. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_CONTROL_TYPE  <br/> |
|Identificador:  <br/> |0x3F02  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Tabla para mostrar MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad puede tener exactamente uno de los siguientes valores:
    
DTCT_LABEL (0x00000000)
  
> Etiqueta de cuadro de diálogo.
   
DTCT_EDIT (0x00000001)
  
> Cuadro de texto de edición de cuadro de diálogo.

DTCT_LBX (0x00000002)
  
> Cuadro de lista de cuadros de diálogo.
    
DTCT_COMBOBOX (0x00000003)
  
> Cuadro combinado de diálogo.

DTCT_DDLBX (0x00000004)
  
> Cuadro de lista desplegable de cuadro de diálogo.

DTCT_CHECKBOX (0x00000005)
  
> Casilla de diálogo.

DTCT_GROUPBOX (0x00000006)
  
> Cuadro de diálogo.
  
DTCT_BUTTON (0x00000007)
  
> Un control de botón de cuadro de diálogo.
    
DTCT_PAGE (0x00000008)
  
> Página con pestañas de cuadro de diálogo.
    
DTCT_RADIOBUTTON (0x00000009)
  
> Botón de radio de cuadro de diálogo.
    
DTCT_MVLISTBOX (0x0000000B)
  
> Un cuadro de lista multivalor rellenado por una propiedad multivalor de tipo string.
    
DTCT_MVDDLBX (0x0000000C)
  
> Un cuadro de lista desplegable multivalor rellenado por una propiedad multivalor de tipo string.
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
mapitags.h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

