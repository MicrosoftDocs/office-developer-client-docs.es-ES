---
title: Tipos e identificadores de propiedad
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 39a5c97c-5ac8-47a8-b193-a4b3ba6a02a5
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 423992e0485e8e3092cfc4126164576906d51149
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567067"
---
# <a name="property-identifiers-and-types"></a>Tipos e identificadores de propiedad

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Todas las propiedades MAPI se representan mediante las etiquetas de propiedad. Una etiqueta de propiedad es un valor entero sin signo de 32 bits que contiene el identificador de la propiedad en la alta pedidos 16 bits y el tipo de propiedad en la baja pedidos 16 bits. Etiquetas de propiedad para todas las propiedades definidas por MAPI se incluyen en el archivo de encabezado mapitags.h.
  
Identificadores de propiedad se usan para indicar qué se usa una propiedad y quién es responsable de ella. Identificadores de propiedad se dividen por MAPI en intervalos; donde se encuentra un identificador en el intervalo indica su uso y la propiedad. 
  
Tipos de propiedad se usan para indicar el formato de datos de la propiedad. MAPI define todos los tipos válidos. Los clientes y proveedores de servicios de creación de nuevas propiedades deben usar uno de estos tipos. Todos los tipos de propiedad se incluyen en el archivo de encabezado mapidefs.h.
  

