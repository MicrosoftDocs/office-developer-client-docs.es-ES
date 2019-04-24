---
title: Identificadores de entrada MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 84c37696-da7a-42e0-b8c0-29658a6c9a48
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 4c414b9f8a1d70fd5eea94da326674a749ccefe2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297882"
---
# <a name="mapi-entry-identifiers"></a>Identificadores de entrada MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los identificadores de entrada son partes de datos binarios almacenados en una estructura [EntryID](entryid.md) que se usan para identificar y abrir de forma única un objeto MAPI. La mayoría de los objetos MAPI tienen identificadores de entrada. Los identificadores de entrada de objetos son análogos a los nombres de archivo de los archivos. Sin embargo, no se pueden transmitir y no se pueden usar en sistemas que no sean el sistema en el que se han originado. 
  
## <a name="entry-identifiers"></a>Identificadores de entrada

Los proveedores de almacenamiento de mensajes asignan identificadores de entrada a los almacenes de mensajes, carpetas y mensajes; los proveedores de la libreta de direcciones los asignan a contenedores de libretas de direcciones, listas de distribución y usuarios de mensajería. Los identificadores de entrada también se usan para abrir un objeto representado por una fila en una tabla, como un objeto status en la tabla de estado. Los objetos almacenan sus identificadores de **** entrada en su propiedad[PidTagEntryId](pidtagentryid-canonical-property.md)(en inglés). 
  
Mientras que los proveedores de servicios crean, asignan y examinan identificadores de entrada, las aplicaciones cliente solo los usan como herramientas para abrir objetos. Para los clientes, los identificadores de entrada son partes opacas de datos binarios y no tienen nada que hacer con el sistema de mensajería subyacente. 
  
Los clientes llaman al método [IMAPIProp:: GetProps](imapiprop-getprops.md) del objeto para recuperar **** su propiedad o el método [IMAPITable:: QueryColumns](imapitable-querycolumns.md) para recuperar la columna que contiene la propiedad de **** una tabla. 
  
Los identificadores de entrada se pasan como parámetros a los métodos **OpenEntry** y **CompareEntryIDs** . Varios objetos MAPI implementan los métodos **OpenEntry** y **CompareEntryIDs** . Con **OpenEntry**, los clientes pueden abrir un objeto. Con **CompareEntryIDs**, los clientes pueden comparar dos identificadores de entrada para determinar si hacen referencia al mismo objeto. Como los identificadores de entrada no son necesariamente comparables binarios, los clientes deben compararlos con el método **CompareEntryIDs** . 
  
Los clientes deben pasar siempre los identificadores de entrada con alineación natural en sus llamadas a los proveedores de servicios, ya que, aunque los proveedores de servicios deben controlar los identificadores de entrada que se alinean arbitrariamente, este no es siempre el caso. Una dirección de memoria con una alineación natural permite al equipo tener acceso a cualquier tipo de datos que admite en esa dirección sin generar un error de alineación. El factor de alineación natural suele ser el mismo factor de alineación usado por el asignador de memoria del sistema y suele ser de 8 bytes.
  
Los identificadores de entrada vienen en dos tipos: corto y largo plazo. Los identificadores de entrada a corto plazo son más rápidos, pero su exclusividad solo se garantiza durante la vida de la sesión actual en la estación de trabajo actual. Los identificadores de entrada a largo plazo tienen una duración más prolongada. Los identificadores de entrada a corto plazo se usan principalmente para las filas de las tablas y las entradas de los cuadros de diálogo, mientras que los identificadores de entrada a largo plazo se usan para muchos objetos como mensajes, carpetas y listas de distribución.
  
## <a name="see-also"></a>Vea también



[Desarrollo de aplicaciones de MAPI](mapi-application-development.md)

