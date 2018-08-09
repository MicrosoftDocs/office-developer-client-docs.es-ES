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
ms.openlocfilehash: e485079de800c63b02d71b3c3ccb90d66101c64b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818146"
---
# <a name="mapi-interfaces"></a>Interfaces MAPI

  
  
**Hace referencia a**: Outlook 
  
La documentación para cada interfaz consta de una sección introductoria que incluye una breve descripción del propósito de la interfaz seguido de una tabla que contiene la información siguiente.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |El archivo de encabezado donde se define la interfaz de y que se debe incluir al compilar el código fuente.  <br/> |
|Expuestos por:  <br/> |El objeto que expone la interfaz.  <br/> |
|Se implementa mediante:  <br/> |Una lista de los componentes que proporcionan una implementación de la interfaz.  <br/> |
|Llamado por:  <br/> |Una lista de los componentes que normalmente se llama a los métodos de la interfaz.  <br/> |
|Identificador de interfaz:  <br/> |El identificador GUID de interfaz.  <br/> |
|Tipo de puntero:  <br/> |El tipo de puntero para el objeto que expone la interfaz.  <br/> |
|Modelo de transacciones:  <br/> |Para las interfaces derivadas de [IMAPIProp](imapipropiunknown.md). Si nontransacted, los cambios surtan efecto inmediatamente; Si se negocian, cambios no tendrán efecto hasta que se llama [IMAPIProp::SaveChanges](imapiprop-savechanges.md) .  <br/> |
   
Después de la primera tabla es otra tabla que enumera todos los métodos de esta interfaz en orden vtable. Un vtable es una matriz de punteros a función creado por el compilador que contiene un puntero a una función para cada método de un objeto MAPI. Se enumeran los métodos en el mismo orden en que se declaran. Métodos heredados de otras interfaces no se muestran en la tabla de orden Vtable, pero pueden usarse de la misma manera, tal como se describe en la interfaz que los define.
  
Después de cada tema de la interfaz, los métodos de la interfaz, a continuación, se documentan en orden alfabético. Para cada método, la documentación incluye una instrucción breve propósito, un bloque de sintaxis y la siguiente información.
  
|**Encabezado**|**Contenido**|
|:-----|:-----|
|Parámetros  <br/> |Una descripción de cada parámetro en el método.  <br/> |
|Valor devuelto  <br/> |Una descripción de los valores únicos que el método puede devolver. Estos son los valores que se deben proteger los autores de llamadas para su código.  <br/> |
|Comentarios  <br/> |Una descripción de cómo y por qué se usa el método.  <br/> |
|Vea también  <br/> |Referencias cruzadas a otros temas de esta referencia.  <br/> |
   
## <a name="see-also"></a>Vea también



[Referencia MAPI](mapi-reference.md)

