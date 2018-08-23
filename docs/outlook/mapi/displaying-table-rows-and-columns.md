---
title: Mostrar filas y columnas
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 49567a8d-b58d-4636-bead-a1f84b4f111d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: dba7bd1fb7b0ca9bc23dbc45e07f44d0cc0dc8fe
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568143"
---
# <a name="displaying-table-rows-and-columns"></a>Mostrar filas y columnas

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
 Una página de propiedades puede utilizarse por un proveedor de la libreta de direcciones para habilitar a los usuarios definir a los destinatarios de correo electrónico nuevo. 
  
En la tabla para mostrar correspondiente contiene cuatro filas, uno para cada control. Los valores de las columnas que indican la posición son los siguientes.
  
|**Control**|**XPOS**|**YPOS**|**DELTAX**|**DELTAY**|
|:-----|:-----|:-----|:-----|:-----|
|Etiqueta de nombre para mostrar  <br/> |14  <br/> |18  <br/> |49  <br/> |8  <br/> |
|Cuadro de edición de nombre para mostrar  <br/> |76  <br/> |16  <br/> |89  <br/> |12  <br/> |
|Etiqueta de dirección de correo electrónico  <br/> |14  <br/> |42  <br/> |50  <br/> |8  <br/> |
|Cuadro de edición de dirección de correo electrónico  <br/> |76  <br/> |40  <br/> |89  <br/> |12  <br/> |
|Casilla  <br/> |14  <br/> |64  <br/> |90  <br/> |12  <br/> |
   
En esta tabla siguiente sugiere los valores adecuados para el tipo del control, su propiedad **PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md)) y la máscara de bits de indicadores, su propiedad **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)).
  
|**Control**|**Tipo**|**Flags**|
|:-----|:-----|:-----|
|Etiqueta de nombre para mostrar  <br/> |DTCT_LABEL  <br/> |0  <br/> |
|Cuadro de edición de nombre para mostrar  <br/> |DTCT_EDIT  <br/> |DT_EDITABLE | DT_REQUIRED  <br/> |
|Etiqueta de dirección de correo electrónico  <br/> |DTCT_LABEL  <br/> |0  <br/> |
|Cuadro de edición de dirección de correo electrónico  <br/> |DTCT_EDIT  <br/> |DT_EDITABLE | DT_REQUIRED  <br/> |
|Casilla  <br/> |DTCT_CHECKBOX  <br/> |DT_EDITABLE  <br/> |
   
En la tabla final se enumera cada control con el contenido de su estructura de control asociado. Tenga en cuenta que el valor de cada uno de los controles de etiqueta aparece en la memoria inmediatamente después de la estructura.
  
|**Control**|**Estructura**|
|:-----|:-----|
|Etiqueta de nombre para mostrar  <br/> |{sizeof(DTBLLABEL), 0} "Nombre para mostrar:"  <br/> |
|Cuadro de edición de nombre para mostrar  <br/> |{sizeof(DTBLEDIT), 0, 80, PR_DISPLAY_NAME}  <br/> |
|Etiqueta de dirección de correo electrónico  <br/> |{sizeof(DTBLLABEL), 0} "Dirección de correo electrónico:"  <br/> |
|Cuadro de edición de dirección de correo electrónico  <br/> |{sizeof(DTBLEDIT), 0, 80, PR_EMAIL_ADDRESS}  <br/> |
|Casilla  <br/> |PR_SEND_RICH_INFO  <br/> |
   
> [!NOTE]
> Los botones **Aceptar**, **Cancelar**y **Ayuda** no se incluyen en la tabla para mostrar. La interfaz de usuario puede agregar el contexto a un cuadro de diálogo mediante la adición de controles no está en la tabla para mostrar. 
  
## <a name="see-also"></a>Recursos adicionales



[Implementación de la tabla para mostrar](display-table-implementation.md)

