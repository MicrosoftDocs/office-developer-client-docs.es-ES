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
ms.openlocfilehash: b7c1ce8d0338a2bda63a276628bdd6e8be3b8eb1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318070"
---
# <a name="attdate-attributes"></a>Atributos attDate

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Todas las propiedades MAPI relativas a las fechas y horas se asignan a los atributos TNEF que tienen el prefijo **attDate** . Todas están codificadas como estructuras **DTR** . Las fechas y las horas de los atributos de datos adjuntos se codifican también como estructuras **DTR** . 
  
Todas las propiedades MAPI relativas a las fechas y horas se asignan a los atributos TNEF que tienen el prefijo **attDate** . Todas están codificadas como estructuras **DTR** . Las fechas y las horas de los atributos de datos adjuntos se codifican también como estructuras **DTR** . 
  
Una estructura **DTR** es muy similar a la estructura **SYSTEMTIME** definida en los archivos de encabezado de Win32. La estructura **DTR** se codifica en la secuencia TNEF como bytes **sizeof (DTR)** a partir del primer miembro de la estructura. La estructura **DTR** se define en la TNEF. H archivo de encabezado. 
  

