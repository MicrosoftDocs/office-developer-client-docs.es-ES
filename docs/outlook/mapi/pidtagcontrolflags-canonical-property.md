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
ms.openlocfilehash: 099f08876eadc83ebb66b9e4226eeeee6277bf01
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331867"
---
# <a name="pidtagcontrolflags-canonical-property"></a>Propiedad canónica PidTagControlFlags

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una máscara de máscara de marcas que gobiernan el comportamiento de un control usado en un cuadro de diálogo generado a partir de una tabla de presentación.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_CONTROL_FLAGS  <br/> |
|Identificador:  <br/> |0x3F00  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Tabla de visualización de MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Se pueden establecer uno o varios de los siguientes indicadores para esta propiedad:
  
DT_ACCEPT_DBCS 
  
> El control puede contener caracteres de un juego de caracteres de doble byte (DBCS). Esta marca se usa con controles de edición. Permite juegos de caracteres de varios bytes.
    
DT_EDITABLE 
  
> Se puede editar el control; se puede cambiar el valor asociado al control. Si no se establece esta marca, el control es de sólo lectura. Este valor se omite en los controles de etiqueta, cuadro de grupo, botón de comando estándar, cuadro de lista desplegable de varios valores y cuadro de lista.
    
DT_MULTILINE 
  
> El control de edición puede contener varias líneas. Esto significa que se puede escribir un carácter de retorno en el control. Esta marca solo es válida para los controles de edición.
    
DT_PASSWORD_EDIT 
  
> Se aplica a los controles de edición. El control de edición se trata como una contraseña. El valor se muestra con asteriscos en lugar de repetir los caracteres reales especificados.
    
DT_REQUIRED 
  
> Si el control permite cambios (DT_EDITABLE), debe tener un valor antes de llamar a [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) . 
    
DT_SET_IMMEDIATE 
  
> Habilita la configuración inmediata de un valor; en cuanto cambia un valor en el control, MAPI llama al método **SetProps** para la propiedad asociada a ese control. Si no se establece esta marca, los valores se establecen cuando se descarta el cuadro de diálogo. 
    
DT_SET_SELECTION 
  
> Cuando se realiza una selección en el cuadro de lista, la columna índice de ese cuadro de lista se establece como una propiedad. Siempre se usa con DT_SET_IMMEDIATE.
    
Esta propiedad se almacena en el miembro ulCtlFlags de la estructura [DTCTL](dtctl.md) de un control. La mayoría de las marcas de control se aplican a todos los controles que permiten la entrada del usuario; algunos sólo se aplican al control de edición. Los controles que no permiten la entrada del usuario, como un botón o una etiqueta, establecen 0 para sus indicadores de control. 
  
Muchos de los valores de indicador se explican por sí mismos. Por ejemplo, cuando DT_REQUIRED se establece para un control, debe contener un valor antes de que se pueda desechar el cuadro de diálogo. El proveedor de servicios puede proporcionar un valor a través de su implementación de **IMAPIProp** o el usuario puede escribir uno. DT_EDITABLE indica que se puede modificar el valor del control. DT_MULTILINE permite que el valor de un control de edición abarque varias líneas. 
  
Algunas marcas de control no son tan obvias en su significado. Cuando un control establece la marca DT_SET_IMMEDIATE, cualquier cambio en su valor surte efecto en cuanto el usuario se mueve a un nuevo control. MAPI realiza una única llamada al método [IMAPIProp:: SetProps](imapiprop-setprops.md) de la interfaz de la propiedad para la propiedad del control. Esto es diferente del comportamiento predeterminado, que consiste en posponer que los cambios en los valores de los controles surtan efecto hasta que el usuario seleccione el botón **Aceptar** o cierre el cuadro de diálogo. La marca DT_SET_IMMEDIATE se suele usar en combinación con las notificaciones de tabla de visualización. 
  
En la siguiente tabla se enumeran los tipos de controles y todos los valores de marca que se pueden establecer para cada tipo.
  
|**Control**|**Valores válidos para esta propiedad**|
|:-----|:-----|
|Botón  <br/> |Debe ser cero  <br/> |
|Casilla  <br/> |DT_EDITABLE, DT_SET_IMMEDIATE  <br/> |
|Cuadro combinado  <br/> |DT_EDITABLE, DT_REQUIRED, DT_SET_IMMEDIATE  <br/> |
|Cuadro de lista desPlegable  <br/> |DT_EDITABLE, DT_SET_IMMEDIATE  <br/> |
|Editar  <br/> |DT_ACCEPT_DBCS, DT_MULTILINE, DT_EDITABLE, DT_PASSWORD_EDIT, DT_REQUIRED, DT_SET_IMMEDIATE  <br/> |
|Cuadro de grupo  <br/> |Debe ser cero  <br/> |
|Label  <br/> |Debe ser cero  <br/> |
|Cuadro de lista  <br/> |Debe ser cero  <br/> |
|Cuadro de lista desplegable multivalor  <br/> |Debe ser cero  <br/> |
|Cuadro de lista multivalor  <br/> |Debe ser cero  <br/> |
|Página con fichas  <br/> |Debe ser cero  <br/> |
|Botón de opción  <br/> |Debe ser cero  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags. h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

