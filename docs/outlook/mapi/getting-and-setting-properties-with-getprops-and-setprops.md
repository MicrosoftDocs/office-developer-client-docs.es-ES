---
title: Obtener y establecer propiedades con GetProps y SetProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 309d2b3d-dc71-4222-b293-4bfc467b5429
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 7d11f69c6da8560f5879ebc38498d852486bed8b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299401"
---
# <a name="getting-and-setting-properties-with-getprops-and-setprops"></a>Obtener y establecer propiedades con GetProps y SetProps
 
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Siempre que sea posible, intente recuperar o modificar una propiedad con los [métodos IMAPIProp::GetProps](imapiprop-getprops.md) e [IMAPIProp::SetProps.](imapiprop-setprops.md) A menos que la propiedad con la que está trabajando sea muy grande, estos métodos deben ser adecuados. La otra alternativa es leer o escribir en una secuencia con la [interfaz IStream.](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) Secuencias controlar propiedades muy grandes correctamente, pero son un mayor vaciado de recursos porque requieren las bibliotecas COM. Use la **interfaz IStream** solo después de que se produce un error en la llamada a **IMAPIProp::GetProps** o **IMAPIProp::SetProps.** 
  

