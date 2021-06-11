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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432264"
---
# <a name="getting-and-setting-multiple-properties"></a>Obtener y establecer varias propiedades

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Al obtener y establecer tantas propiedades como sea posible con el menor número de llamadas, se reduce la actividad remota y se reduce la sobrecarga que implica cada propiedad. Aunque los proveedores de servicios intentan recopilar propiedades antes de realizar una llamada de procedimiento remoto para la recuperación o modificación, puede optimizar este esfuerzo solicitando varias propiedades para empezar.
  
Por ejemplo, si trabaja con listas de enrutamiento que describen destinatarios futuros con propiedades con nombre pertenecientes a determinados conjuntos de propiedades, procese todos los destinatarios con dos llamadas. Use una llamada a [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) para recuperar los identificadores de todas las propiedades del destinatario y la otra llamada a [IMAPIProp::GetProps](imapiprop-getprops.md) para recuperar todos los valores. La alternativa, realizar una llamada a **GetIDsFromNames** seguida de una llamada a **GetProps** para cada destinatario, es mucho menos eficiente. 
  

