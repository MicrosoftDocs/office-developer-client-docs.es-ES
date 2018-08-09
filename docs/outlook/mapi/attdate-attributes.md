---
title: Atributos attDate
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22801641-752c-4c81-be90-02039eaa4277
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: f3319c9ae49fa97a6179b0ee800bd5dd594aefab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816464"
---
# <a name="attdate-attributes"></a>Atributos attDate

  
  
**Hace referencia a**: Outlook 
  
Todas las propiedades MAPI relativas a las fechas y horas se asignan a los atributos TNEF que tienen el prefijo **attDate** . Estos se codifican como estructuras **DTR** . Las fechas y horas para los atributos de los datos adjuntos se codifican como así como las estructuras **DTR** . 
  
Todas las propiedades MAPI relativas a las fechas y horas se asignan a los atributos TNEF que tienen el prefijo **attDate** . Estos se codifican como estructuras **DTR** . Las fechas y horas para los atributos de los datos adjuntos se codifican como así como las estructuras **DTR** . 
  
Una estructura **DTR** es muy similar a la estructura **SYSTEMTIME** definida en los archivos de encabezado de Win32. La estructura **DTR** está codificada en la secuencia TNEF como bytes **sizeof(DTR)** empezando por el primer miembro de la estructura. La estructura **DTR** se define en el TNEF. Archivo de encabezado H. 
  

