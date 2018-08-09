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
ms.openlocfilehash: d8c6699ac1bc5687b1c885d156535e5b54b93140
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816461"
---
# <a name="attattachrenddata"></a>attAttachRenddata

  
  
**Hace referencia a**: Outlook 
  
El atributo **attAttachRenddata** se codifica como una estructura **RENDDATA** que se describe cómo y dónde se representan los datos adjuntos en el texto del mensaje. La estructura **RENDDATA** simplemente está codificada en la secuencia TNEF como bytes **sizeof(RENDDATA)** que comienzan con el primer miembro de la estructura **RENDDATA** . Si se establece el valor de miembro de **dwFlags** de la estructura **RENDDATA** en **MAC_BINARY**, a continuación, se almacenan los datos para los datos adjuntos siguientes en formato MacBinary; de lo contrario, los datos adjuntos se codifican como de costumbre.
  

