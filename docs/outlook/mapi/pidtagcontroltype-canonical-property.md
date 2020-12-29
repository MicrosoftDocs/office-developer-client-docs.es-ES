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
  
Contiene un valor que indica un tipo de control para un control utilizado en un cuadro de diálogo. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_CONTROL_TYPE  <br/> |
|Identificador:  <br/> |0x3F02  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Tabla de visualización de MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad puede tener exactamente uno de los siguientes valores:
    
DTCT_LABEL (0x00000000)
  
> Una etiqueta de cuadro de diálogo.
   
DTCT_EDIT (0x00000001)
  
> Un cuadro de texto de edición de cuadro de diálogo.

DTCT_LBX (0x00000002)
  
> Un cuadro de lista de cuadro de diálogo.
    
DTCT_COMBOBOX (0x00000003)
  
> Cuadro combinado de cuadro de diálogo.

DTCT_DDLBX (0x00000004)
  
> Cuadro de lista desplegable de cuadro de diálogo.

DTCT_CHECKBOX (0x00000005)
  
> Casilla de verificación de cuadro de diálogo.

DTCT_GROUPBOX (0x00000006)
  
> Un cuadro de grupo de diálogo.
  
DTCT_BUTTON (0x00000007)
  
> Un control botón de cuadro de diálogo.
    
DTCT_PAGE (0x00000008)
  
> Una página con fichas de cuadro de diálogo.
    
DTCT_RADIOBUTTON (0x00000009)
  
> Un botón de opción del cuadro de diálogo.
    
DTCT_MVLISTBOX (0x0000000B)
  
> Un cuadro de lista multivalor rellenado por una propiedad multivalor de tipo String.
    
DTCT_MVDDLBX (0x0000000C)
  
> Un cuadro de lista desplegable multivalor rellenado por una propiedad multivalor de tipo String.
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
mapitags. h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Recursos adicionales



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

