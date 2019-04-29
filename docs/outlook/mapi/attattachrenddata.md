---
title: attAttachRenddata
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c510b7a5-0f55-46af-bddb-40a8195a84d4
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: d58fc0eae5401773d28f5bbe510913ff381ade8d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427139"
---
# <a name="attattachrenddata"></a>attAttachRenddata

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
El atributo **attAttachRenddata** se codifica como una estructura **RENDDATA** que describe cómo y dónde se representan los datos adjuntos en el texto del mensaje. La estructura **RENDDATA** se codifica simplemente en la secuencia TNEF como bytes **sizeof (RENDDATA)** , comenzando por el primer miembro de la estructura **RENDDATA** . Si el valor del miembro **dwFlags** de la estructura **RENDDATA** se establece en **MAC_BINARY**, los datos de los siguientes datos adjuntos se almacenan en formato MacBinary; de lo contrario, los datos adjuntos se codifican de la forma habitual.
  

