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
ms.openlocfilehash: 88c3e0bdb3cc6660e35faf62c5bb63ec2f6352bc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590375"
---
# <a name="getting-and-setting-multiple-properties"></a>Obtener y establecer varias propiedades

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Para obtener y establecer propiedades tantos como sea posible con el menor número de llamadas, remotas actividad es reducida y se reduce la sobrecarga que implica con cada propiedad. Aunque los proveedores de servicios intentan recopilar propiedades antes de realizar una llamada a procedimiento remoto para la recuperación o modificación, puede optimizar este esfuerzo solicitando varias propiedades para empezar.
  
Por ejemplo, si trabaja con listas de enrutamiento que describen a los destinatarios futuros con las propiedades con nombre que pertenecen a conjuntos de propiedades determinado, proceso de todos los destinatarios con dos llamadas. Utilice una llamada a [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) para recuperar los identificadores de todas las propiedades del destinatario y la otra llamada a [IMAPIProp::GetProps](imapiprop-getprops.md) para recuperar todos los valores. La alternativa, realizar una llamada a **a GetIDsFromNames** seguido de una llamada a **GetProps** para cada destinatario, es mucho menos eficaz. 
  

