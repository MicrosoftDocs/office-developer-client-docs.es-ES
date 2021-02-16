---
title: Identificadores y tipos de propiedad
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 39a5c97c-5ac8-47a8-b193-a4b3ba6a02a5
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: caba60b7059d1c1f8f0440aeb55abb88801fbc9a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437220"
---
# <a name="property-identifiers-and-types"></a>Identificadores y tipos de propiedad

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Todas las propiedades MAPI se representan mediante etiquetas de propiedad. Una etiqueta de propiedad es un valor entero sin signo de 32 bits que contiene el identificador de la propiedad en el orden alto 16 bits y el tipo de la propiedad en el orden bajo 16 bits. Las etiquetas de propiedad de todas las propiedades definidas por MAPI se incluyen en el archivo de encabezado mapitags.h.
  
Los identificadores de propiedad se usan para indicar para qué se usa una propiedad y quién es responsable de ella. Los identificadores de propiedad se dividen por MAPI en intervalos; donde un identificador se encuentra en el intervalo indica su uso y propiedad. 
  
Los tipos de propiedad se usan para indicar el formato de los datos de la propiedad. MAPI define todos los tipos válidos. Los clientes y proveedores de servicios que crean nuevas propiedades deben usar uno de estos tipos. Todos los tipos de propiedad se incluyen en el archivo de encabezado mapidefs.h.
  

