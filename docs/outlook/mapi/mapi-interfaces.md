---
title: Interfaces MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: 34a66cf0-b4e0-4fd5-b937-cd157888961d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 4f5d6a5d2dbb48a86363896bf14b61ed28118330
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422666"
---
# <a name="mapi-interfaces"></a>Interfaces MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La documentación de cada interfaz consta de una sección introductoria que incluye una breve descripción del propósito de la interfaz seguida de una tabla que contiene la siguiente información.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |El archivo de encabezado donde se define la interfaz y que debe incluirse al compilar el código fuente.  <br/> |
|Expuesto por:  <br/> |Objeto que expone la interfaz.  <br/> |
|Implementado por:  <br/> |Una lista de los componentes que proporcionan una implementación de la interfaz.  <br/> |
|Llamado por:  <br/> |Una lista de los componentes que normalmente llaman a los métodos de la interfaz.  <br/> |
|Identificador de interfaz:  <br/> |GUID del identificador de interfaz.  <br/> |
|Tipo de puntero:  <br/> |Tipo de puntero para el objeto que expone la interfaz.  <br/> |
|Modelo de transacción:  <br/> |Para interfaces derivadas de [IMAPIProp](imapipropiunknown.md). Si no se transirán, los cambios se realizarán inmediatamente; si se realizan transacciones, los cambios no tienen efecto hasta que se llama a [IMAPIProp::SaveChanges.](imapiprop-savechanges.md)  <br/> |
   
Después de la primera tabla hay otra tabla que enumera todos los métodos de esta interfaz en orden de tabla virtual. Una tabla virtual es una matriz de punteros de función creada por el compilador que contiene un puntero de función para cada método de un objeto MAPI. Los métodos se enumeran en el mismo orden en que se declaran. Los métodos heredados de otras interfaces no se muestran en la tabla Orden de tabla virtual, pero se pueden usar de la misma manera que se documenta en la interfaz que los define.
  
Después de cada tema de la interfaz, los métodos de la interfaz se documentan en orden alfabético. Para cada método, la documentación incluye una instrucción de propósito breve, un bloque de sintaxis y la siguiente información.
  
|**Título**|**Contenido**|
|:-----|:-----|
|Parámetros  <br/> |Descripción de cada parámetro del método.  <br/> |
|Valor devuelto  <br/> |Descripción de los valores únicos que puede devolver el método. Estos son los valores que los autores de llamadas deben comprobar en su código.  <br/> |
|Comentarios  <br/> |Una descripción de por qué y cómo se usa el método.  <br/> |
|Consulte también  <br/> |Referencias cruzadas a otros temas de esta referencia.  <br/> |
   
## <a name="see-also"></a>Vea también



[Referencia MAPI](mapi-reference.md)

