---
title: Obtener y establecer varias propiedades
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 29b7f5f1-afc1-45d9-8867-9312c072e74b
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: dd25751978eb036531238e6372e35934b3ec145a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299380"
---
# <a name="getting-and-setting-multiple-properties"></a>Obtener y establecer varias propiedades

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Al obtener y establecer tantas propiedades como sea posible con el menor número de llamadas, se reduce la actividad remota y se reduce la sobrecarga que supone cada propiedad. Aunque los proveedores de servicios intentan recopilar propiedades antes de realizar una llamada a procedimiento remoto para la recuperación o modificación, puede optimizar este esfuerzo solicitando que se inicien varias propiedades.
  
Por ejemplo, si trabaja con listas de enrutamiento que describen futuros destinatarios con propiedades con nombre que pertenecen a conjuntos de propiedades en particular, procese todos los destinatarios con dos llamadas. Use una llamada a [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) para recuperar los identificadores de todas las propiedades del destinatario y la otra llamada a [IMAPIProp:: GetProps](imapiprop-getprops.md) para recuperar todos los valores. La alternativa, al realizar una llamada a **GetIDsFromNames** seguida de una llamada a **GetProps** para cada destinatario, es mucho menos eficaz. 
  

