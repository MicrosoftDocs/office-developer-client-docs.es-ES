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
ms.openlocfilehash: b8212f4a055125858b77ee615a5d929a4a62bb82
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818107"
---
# <a name="mapi-entry-identifiers"></a>Identificadores de entrada MAPI

  
  
**Hace referencia a**: Outlook 
  
Los identificadores de entrada son fragmentos de datos binarios almacenados en una estructura de [ENTRYID](entryid.md) que se usan para identificar de forma exclusiva y abrir un objeto MAPI. La mayoría de los objetos MAPI tiene los identificadores de entrada. Los identificadores de entrada para los objetos son similares a los nombres de archivo para los archivos. Sin embargo, que no están transmisible y no pueden usarse en sistemas que no sea el sistema que se originan en. 
  
## <a name="entry-identifiers"></a>Identificadores de entrada

Los proveedores de almacén de mensajes asignan los identificadores de entrada a los almacenes de mensajes, carpetas y mensajes; los proveedores de la libreta de direcciones asignan a contenedores de la libreta de direcciones, listas de distribución y usuarios de mensajería. Los identificadores de entrada también se usan para abrir un objeto representado por una fila en una tabla, como un objeto de estado en la tabla de estado. Los objetos almacenan sus identificadores de entrada en su propiedad de **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)). 
  
Mientras que los proveedores de servicios de creación, asignan y examinan los identificadores de entrada, las aplicaciones cliente los usan sólo como herramientas para abrir objetos. A los clientes, los identificadores de entrada son piezas opacos de datos binarios y no tienen nada que ver con el sistema de mensajería subyacente. 
  
Los clientes llamar a un método del objeto [IMAPIProp::GetProps](imapiprop-getprops.md) para recuperar su propiedad de **entrada del objeto** o el método de [IMAPITable::QueryColumns](imapitable-querycolumns.md) de una tabla para recuperar la columna que contiene la propiedad de **entrada del objeto** . 
  
Los identificadores de entrada se pasan como parámetros a los métodos **OpenEntry** y **CompareEntryIDs** . Varios objetos MAPI implementan los métodos **OpenEntry** y **CompareEntryIDs** . Con **OpenEntry**, los clientes pueden abrir un objeto. Con **CompareEntryIDs**, los clientes pueden comparar dos identificadores de entrada para determinar si hacen referencia al mismo objeto. Debido a que los identificadores de entrada no son necesariamente binarios comparable, los clientes deben compararlos por el método **CompareEntryIDs** . 
  
Los clientes siempre deben pasar los identificadores de entrada con naturalidad alineado en sus llamadas a proveedores de servicios, ya que aunque los proveedores de servicios deben administrar los identificadores de entrada que se alinean arbitrariamente, esto no siempre es el caso. Una dirección de memoria con naturalidad alineado permite que el equipo tener acceso a cualquier tipo de datos que admite en esa dirección sin que se genere un error de alineación. El factor de alineación natural es normalmente el mismo factor de alineación usado por el asignador de memoria del sistema y normalmente es de 8 bytes.
  
Los identificadores de entrada se incluyen en dos tipos: a corto plazo y a largo plazo. Los identificadores de entrada a corto plazo son más rápidas construir, pero se garantiza su unicidad sólo a través de la vida de la sesión actual en la estación de trabajo actual. Los identificadores de entrada a largo plazo tienen un ciclo de vida más prolongado. Los identificadores de entrada a corto plazo se usan principalmente para las filas en las tablas y las entradas de los cuadros de diálogo, mientras que los identificadores de entrada a largo plazo se usan para muchos objetos, como mensajes, carpetas y listas de distribución.
  
## <a name="see-also"></a>Vea también



[Desarrollo de aplicaciones de MAPI](mapi-application-development.md)

