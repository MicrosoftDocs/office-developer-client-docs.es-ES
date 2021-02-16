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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430885"
---
# <a name="pidtagcontrolflags-canonical-property"></a>Propiedad canónica PidTagControlFlags

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una máscara de bits de marcas que rigen el comportamiento de un control usado en un cuadro de diálogo creado a partir de una tabla para mostrar.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_CONTROL_FLAGS  <br/> |
|Identificador:  <br/> |0x3F00  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Tabla para mostrar MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Se pueden establecer una o varias de las siguientes marcas para esta propiedad:
  
DT_ACCEPT_DBCS 
  
> El control puede tener Double-Byte juego de caracteres (DBCS) en él. Esta marca se usa con controles de edición. Permite juegos de caracteres de varios bytes.
    
DT_EDITABLE 
  
> El control se puede editar; se puede cambiar el valor asociado con el control. Cuando no se establece esta marca, el control es de solo lectura. Este valor se omite en los controles de etiqueta, cuadro de grupo, botón de inserción estándar, cuadro de lista desplegable multivalor y cuadro de lista.
    
DT_MULTILINE 
  
> El control de edición puede contener varias líneas. Esto significa que se puede especificar un carácter devuelto dentro del control. Esta marca solo es válida para controles de edición.
    
DT_PASSWORD_EDIT 
  
> Se aplica a controles de edición. El control de edición se trata como una contraseña. El valor se muestra con asteriscos en lugar de hacer eco de los caracteres reales especificados.
    
DT_REQUIRED 
  
> Si el control permite cambios (DT_EDITABLE), debe tener un valor antes de llamar a [IMAPIProp::SaveChanges.](imapiprop-savechanges.md) 
    
DT_SET_IMMEDIATE 
  
> Habilita la configuración inmediata de un valor; Tan pronto como cambia un valor en el control, MAPI llama al **método SetProps** para la propiedad asociada con ese control. Cuando no se establece esta marca, los valores se establecen cuando se descarta el cuadro de diálogo. 
    
DT_SET_SELECTION 
  
> Cuando se realiza una selección dentro del cuadro de lista, la columna de índice de ese cuadro de lista se establece como una propiedad. Siempre se usa con DT_SET_IMMEDIATE.
    
Esta propiedad se almacena en el miembro ulCtlFlags de la estructura [DTCTL](dtctl.md) de un control. La mayoría de las marcas de control se aplican a todos los controles que permiten la entrada del usuario; algunos se aplican solo al control de edición. Los controles que no permiten la entrada del usuario, como un botón o una etiqueta, establecen 0 para sus marcas de control. 
  
Muchos de los valores de marca se explican por sí solos. Por ejemplo, cuando DT_REQUIRED para un control, debe contener un valor antes de que se pueda descartar el cuadro de diálogo. El proveedor de servicios puede proporcionar un valor a través de su **implementación IMAPIProp** o el usuario puede escribir uno. DT_EDITABLE indica que se puede modificar el valor del control. DT_MULTILINE permite que el valor de un control de edición abarque varias líneas. 
  
Algunas marcas de control no son tan obvias en su significado. Cuando un control establece DT_SET_IMMEDIATE marca, cualquier cambio en su valor tendrá efecto en cuanto el usuario se mueva a un nuevo control. MAPI realiza una sola llamada al método [IMAPIProp::SetProps](imapiprop-setprops.md) de la interfaz de propiedades para la propiedad del control. Esto es diferente del comportamiento predeterminado, que es posponer que los cambios  en los valores de control tengan efecto hasta que el usuario selecciona el botón Aceptar o descarta el cuadro de diálogo. La DT_SET_IMMEDIATE se usa a menudo en combinación con las notificaciones de la tabla de visualización. 
  
En la tabla siguiente se enumeran los tipos de controles y todos los valores de marca que se pueden establecer para cada tipo.
  
|**Control**|**Valores válidos para esta propiedad**|
|:-----|:-----|
|Botón  <br/> |Debe ser cero  <br/> |
|Casilla  <br/> |DT_EDITABLE, DT_SET_IMMEDIATE  <br/> |
|Cuadro combinado  <br/> |DT_EDITABLE, DT_REQUIRED, DT_SET_IMMEDIATE  <br/> |
|Cuadro de lista desplegable  <br/> |DT_EDITABLE, DT_SET_IMMEDIATE  <br/> |
|Editar  <br/> |DT_ACCEPT_DBCS, DT_MULTILINE, DT_EDITABLE, DT_PASSWORD_EDIT, DT_REQUIRED, DT_SET_IMMEDIATE  <br/> |
|Cuadro de grupo  <br/> |Debe ser cero  <br/> |
|Etiqueta  <br/> |Debe ser cero  <br/> |
|Cuadro de lista  <br/> |Debe ser cero  <br/> |
|Cuadro de lista desplegable con varios valores  <br/> |Debe ser cero  <br/> |
|Cuadro de lista de varios valores  <br/> |Debe ser cero  <br/> |
|Página con pestañas  <br/> |Debe ser cero  <br/> |
|Botón de radio  <br/> |Debe ser cero  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Consulte también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

