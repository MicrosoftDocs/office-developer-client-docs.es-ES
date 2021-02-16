---
title: Mostrar filas y columnas de tabla
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 49567a8d-b58d-4636-bead-a1f84b4f111d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f9f1cc0bebf3c90a5c12f2714e8ab7eea59104da
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407119"
---
# <a name="displaying-table-rows-and-columns"></a>Mostrar filas y columnas de tabla

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
 Un proveedor de libreta de direcciones puede usar una página de propiedades para permitir a los usuarios definir nuevos destinatarios de correo electrónico. 
  
La tabla para mostrar correspondiente contiene cuatro filas, una para cada control. Los valores de las columnas que indican la posición son los siguientes.
  
|**Control**|**XPOS**|**YPOS**|**DELTAX**|**DELTAY**|
|:-----|:-----|:-----|:-----|:-----|
|Etiqueta de nombre para mostrar  <br/> |14   <br/> |18   <br/> |49  <br/> |8   <br/> |
|Cuadro de edición de nombre para mostrar  <br/> |76  <br/> |16   <br/> |89  <br/> |12   <br/> |
|Etiqueta de dirección de correo electrónico  <br/> |14   <br/> |42  <br/> |50  <br/> |8   <br/> |
|Cuadro de edición de direcciones de correo electrónico  <br/> |76  <br/> |40  <br/> |89  <br/> |12   <br/> |
|Casilla  <br/> |14   <br/> |64  <br/> |90  <br/> |12   <br/> |
   
En la siguiente tabla se sugieren los valores adecuados para el tipo del control, su propiedad **PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md)) y la máscara de bits de marcas, su propiedad **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)).
  
|**Control**|**Tipo**|**Flags**|
|:-----|:-----|:-----|
|Etiqueta de nombre para mostrar  <br/> |DTCT_LABEL  <br/> |0  <br/> |
|Cuadro de edición de nombre para mostrar  <br/> |DTCT_EDIT  <br/> |DT_EDITABLE | DT_REQUIRED  <br/> |
|Etiqueta de dirección de correo electrónico  <br/> |DTCT_LABEL  <br/> |0  <br/> |
|Cuadro de edición de direcciones de correo electrónico  <br/> |DTCT_EDIT  <br/> |DT_EDITABLE | DT_REQUIRED  <br/> |
|Casilla  <br/> |DTCT_CHECKBOX  <br/> |DT_EDITABLE  <br/> |
   
La tabla final enumera cada control con el contenido de su estructura de control asociada. Observe que el valor de cada uno de los controles de etiqueta aparece en la memoria directamente después de la estructura.
  
|**Control**|**Estructura**|
|:-----|:-----|
|Etiqueta de nombre para mostrar  <br/> |{sizeof(DTBLLABEL), 0} "Nombre para mostrar:"  <br/> |
|Cuadro de edición de nombre para mostrar  <br/> |{sizeof(DTBLEDIT), 0, 80, PR_DISPLAY_NAME}  <br/> |
|Etiqueta de dirección de correo electrónico  <br/> |{sizeof(DTBLLABEL), 0} "Dirección de correo electrónico:"  <br/> |
|Cuadro de edición de direcciones de correo electrónico  <br/> |{sizeof(DTBLEDIT), 0, 80, PR_EMAIL_ADDRESS}  <br/> |
|Casilla  <br/> |PR_SEND_RICH_INFO  <br/> |
   
> [!NOTE]
> Los **botones** Aceptar, **Cancelar** **y Ayuda** no se incluyen en la tabla de presentación. La interfaz de usuario puede agregar contexto a un cuadro de diálogo agregando controles que no están en la tabla para mostrar. 
  
## <a name="see-also"></a>Consulte también



[Implementación de la tabla de visualización](display-table-implementation.md)

