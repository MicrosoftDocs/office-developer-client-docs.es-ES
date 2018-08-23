---
title: Propiedad canónica PidTagControlFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagControlFlags
api_type:
- HeaderDef
ms.assetid: b97a9e72-fbb7-49ab-a19d-5e9bd1b8a80d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: fc47dc88ed0618bcdf46c309776d5a871d2128e9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580743"
---
# <a name="pidtagcontrolflags-canonical-property"></a>Propiedad canónica PidTagControlFlags

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una máscara de bits de indicadores que rigen el comportamiento de un control que se utiliza en un cuadro de diálogo creado a partir de una tabla para mostrar.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_CONTROL_FLAGS  <br/> |
|Identificador:  <br/> |0x3F00  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Tabla MAPI para mostrar  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad se pueden establecer uno o varios de los siguientes indicadores:
  
DT_ACCEPT_DBCS 
  
> El control puede tener caracteres del juego de caracteres de doble Byte (DBCS) en ella. Este indicador se utiliza con controles de edición. Permite que los conjuntos de caracteres de varios bytes.
    
DT_EDITABLE 
  
> El control se puede editar; se puede cambiar el valor asociado al control. Cuando no se establece este indicador, el control es de sólo lectura. Este valor se omite en la etiqueta, cuadro de grupo, botón de comando estándar, multivalor desplegable de un cuadro de lista y controles de cuadro de lista.
    
DT_MULTILINE 
  
> El control de edición puede contener varias líneas. Esto significa que un carácter de retorno puede especificarse dentro del control. Esta marca es válida para sólo controles de edición.
    
DT_PASSWORD_EDIT 
  
> Se aplica a controles de edición. El control de edición se trata como una contraseña. El valor se muestra con asteriscos en lugar de eco de los caracteres reales especificados.
    
DT_REQUIRED 
  
> Si el control permite cambios (DT_EDITABLE), debe tener un valor antes de llamar a [IMAPIProp::SaveChanges](imapiprop-savechanges.md) . 
    
DT_SET_IMMEDIATE 
  
> Permite la configuración de ejecución de un valor; tan pronto como un valor en el control de cambios, MAPI llama al método de **SetProps** para la propiedad asociada a ese control. Cuando no se establece este marcador, se establecen los valores cuando se cierra el cuadro de diálogo. 
    
DT_SET_SELECTION 
  
> Cuando se realiza una selección dentro del cuadro de lista, la columna de índice de ese cuadro de lista se establece como una propiedad. Siempre se utiliza con DT_SET_IMMEDIATE.
    
Esta propiedad se almacena en el miembro ulCtlFlags de la estructura de un control [DTCTL](dtctl.md) . La mayoría de los indicadores de control se aplican a todos los controles que permiten la entrada del usuario; Algunas se aplican sólo para el control de edición. Los controles que no permiten la entrada del usuario, como un botón o una etiqueta, establecen 0 para sus indicadores de control. 
  
Muchos de los valores de indicador son explican por sí solos. Por ejemplo, cuando DT_REQUIRED se establece para un control, debe contener un valor antes de que se permite el cuadro de diálogo para ser descartados. El proveedor de servicios puede proporcionar un valor a través de su implementación de **IMAPIProp** o el usuario puede escribir uno. DT_EDITABLE indica que se puede modificar el valor para el control. DT_MULTILINE permite que el valor de un control de edición abarcar varias líneas. 
  
Algunos indicadores de control no son tan obvias en su significado. Cuando un control establece la marca DT_SET_IMMEDIATE, afecta los cambios en su valor tomar tan pronto como el usuario se mueve a un nuevo control. MAPI realiza una única llamada al método [IMAPIProp::SetProps](imapiprop-setprops.md) de la interfaz de la propiedad para la propiedad del control. Esto es diferente del comportamiento predeterminado, que es posponer la necesidad de los cambios realizados en los valores de control tendrán efecto hasta después de que el usuario selecciona el botón **Aceptar** o cierra el cuadro de diálogo. El indicador DT_SET_IMMEDIATE a menudo se usa en combinación con las notificaciones de tabla para mostrar. 
  
En la siguiente tabla se enumera los tipos de controles y todos los valores de indicador que se pueden establecer para cada tipo.
  
|**Control**|**Valores válidos para esta propiedad**|
|:-----|:-----|
|Botón  <br/> |Debe ser cero  <br/> |
|Casilla  <br/> |DT_EDITABLE, DT_SET_IMMEDIATE  <br/> |
|Cuadro combinado  <br/> |DT_EDITABLE, DT_REQUIRED, DT_SET_IMMEDIATE  <br/> |
|Cuadro de lista desplegable  <br/> |DT_EDITABLE, DT_SET_IMMEDIATE  <br/> |
|Edit  <br/> |DT_ACCEPT_DBCS, DT_MULTILINE, DT_EDITABLE, DT_PASSWORD_EDIT, DT_REQUIRED, DT_SET_IMMEDIATE  <br/> |
|Cuadro de grupo  <br/> |Debe ser cero  <br/> |
|Etiqueta  <br/> |Debe ser cero  <br/> |
|Cuadro de lista  <br/> |Debe ser cero  <br/> |
|Cuadro de lista desplegable con varios valores  <br/> |Debe ser cero  <br/> |
|Cuadro de lista con varios valores  <br/> |Debe ser cero  <br/> |
|Página con fichas  <br/> |Debe ser cero  <br/> |
|Botón de opción  <br/> |Debe ser cero  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Recursos adicionales



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

