---
title: atributos attDate
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22801641-752c-4c81-be90-02039eaa4277
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: b7c1ce8d0338a2bda63a276628bdd6e8be3b8eb1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408281"
---
# <a name="attdate-attributes"></a>atributos attDate

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Todas las propiedades MAPI relacionadas con fechas y horas se asignan a atributos TNEF que tienen el **prefijo attDate.** Todas están codificadas como **estructuras DTR.** Las fechas y horas de los atributos de datos adjuntos también se codifican como estructuras **DTR.** 
  
Todas las propiedades MAPI relacionadas con fechas y horas se asignan a atributos TNEF que tienen el **prefijo attDate.** Todas están codificadas como **estructuras DTR.** Las fechas y horas de los atributos de datos adjuntos también se codifican como estructuras **DTR.** 
  
Una **estructura DTR** es muy similar a la **estructura SYSTEMTIME** definida en los archivos de encabezado de Win32. La **estructura DTR** se codifica en la secuencia TNEF como **bytes sizeof(DTR)** a partir del primer miembro de la estructura. La **estructura DTR** se define en el TNEF. Archivo de encabezado H. 
  

