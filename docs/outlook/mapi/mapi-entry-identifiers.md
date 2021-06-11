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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414966"
---
# <a name="mapi-entry-identifiers"></a>Identificadores de entrada MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los identificadores de entrada son fragmentos de datos binarios almacenados en una [estructura ENTRYID](entryid.md) que se usan para identificar y abrir de forma única un objeto MAPI. La mayoría de los objetos MAPI tienen identificadores de entrada. Los identificadores de entrada de objetos son análogos a los nombres de archivo de los archivos. Sin embargo, no son transmitibles y no se pueden usar en sistemas distintos del sistema en el que se originaron. 
  
## <a name="entry-identifiers"></a>Identificadores de entrada

Los proveedores de almacenes de mensajes asignan identificadores de entrada a almacenes de mensajes, carpetas y mensajes; los proveedores de libretas de direcciones los asignan a contenedores de libreta de direcciones, listas de distribución y usuarios de mensajería. Los identificadores de entrada también se usan para abrir un objeto representado por una fila de una tabla, como un objeto de estado en la tabla de estado. Los objetos almacenan sus identificadores de entrada **PR_ENTRYID** propiedad ([PidTagEntryId](pidtagentryid-canonical-property.md)). 
  
Mientras que los proveedores de servicios crean, asignan y examinan identificadores de entrada, las aplicaciones cliente solo los usan como herramientas para abrir objetos. Para los clientes, los identificadores de entrada son partes opacas de datos binarios y no tienen nada que ver con el sistema de mensajería subyacente. 
  
Los clientes llaman al método [IMAPIProp::GetProps](imapiprop-getprops.md) de un objeto para recuperar su propiedad PR_ENTRYID o el método [IMAPITable::QueryColumns](imapitable-querycolumns.md) de una tabla para recuperar la columna que contiene la **propiedad PR_ENTRYID.**  
  
Los identificadores de entrada se pasan como parámetros a los métodos **OpenEntry** y **CompareEntryIDs.** Varios objetos MAPI implementan los **métodos OpenEntry** y **CompareEntryIDs.** Con **OpenEntry,** los clientes pueden abrir un objeto. Con **CompareEntryIDs,** los clientes pueden comparar dos identificadores de entrada para determinar si hacen referencia al mismo objeto. Dado que los identificadores de entrada no son necesariamente comparables binarios, los clientes deben compararlos mediante el **método CompareEntryIDs.** 
  
Los clientes siempre deben pasar identificadores de entrada alineados de forma natural en sus llamadas a los proveedores de servicios, ya que aunque los proveedores de servicios deben controlar los identificadores de entrada que están alineados arbitrariamente, no siempre es así. Una dirección de memoria alineada de forma natural permite al equipo tener acceso a cualquier tipo de datos que admita en esa dirección sin generar un error de alineación. El factor de alineación natural suele ser el mismo factor de alineación usado por el asignador de memoria del sistema y suele ser de 8 bytes.
  
Los identificadores de entrada se incluyen en dos tipos: a corto plazo y a largo plazo. Los identificadores de entrada a corto plazo son más rápidos de construir, pero su singularidad solo se garantiza durante la vida de la sesión actual en la estación de trabajo actual. Los identificadores de entrada a largo plazo tienen una vida útil más prolongada. Los identificadores de entrada a corto plazo se usan principalmente para filas de tablas y entradas en cuadros de diálogo, mientras que los identificadores de entrada a largo plazo se usan para muchos objetos, como mensajes, carpetas y listas de distribución.
  
## <a name="see-also"></a>Vea también



[Desarrollo de aplicaciones de MAPI](mapi-application-development.md)

