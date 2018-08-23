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
ms.openlocfilehash: a006c126ec5e0fb86847226195efd03f7ae5351f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569452"
---
# <a name="attattachrenddata"></a>attAttachRenddata

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
El atributo **attAttachRenddata** se codifica como una estructura **RENDDATA** que se describe cómo y dónde se representan los datos adjuntos en el texto del mensaje. La estructura **RENDDATA** simplemente está codificada en la secuencia TNEF como bytes **sizeof(RENDDATA)** que comienzan con el primer miembro de la estructura **RENDDATA** . Si se establece el valor de miembro de **dwFlags** de la estructura **RENDDATA** en **MAC_BINARY**, a continuación, se almacenan los datos para los datos adjuntos siguientes en formato MacBinary; de lo contrario, los datos adjuntos se codifican como de costumbre.
  

