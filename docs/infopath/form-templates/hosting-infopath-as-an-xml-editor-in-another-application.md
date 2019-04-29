---
title: Hospedar InfoPath como un editor XML en otra aplicación
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ae24b317-f486-763a-7009-e32c5cb85b59
description: El entorno de edición de formularios de Microsoft InfoPath se puede hospedar en una aplicación para Windows personalizada, lo que permite a los programadores integrar el entorno de edición de formularios de InfoPath en aplicaciones de línea de negocio.
ms.openlocfilehash: b85e47d506b17982bb883c9d56ea13131807d1cf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422582"
---
# <a name="hosting-infopath-as-an-xml-editor-in-another-application"></a>Hospedar InfoPath como un editor XML en otra aplicación

El entorno de edición de formularios de Microsoft InfoPath puede hospedarse en una aplicación para Windows personalizada. Esta característica permite a los programadores integrar el entorno de edición de formularios de InfoPath en las aplicaciones de la línea de negocio. Los programadores que crean aplicaciones tradicionales basadas en COM pueden usar el objeto **InfoPathEditorObject**, disponible si se hace referencia a IPEDITOR.DLL, y los programadores que escriben aplicaciones basadas en Microsoft .NET pueden usar el ensamblado **Microsoft.Office.InfoPath.FormControl**, que proporciona tipos administrados basados en la interfaz COM. El archivo IPEDITOR.DLL y el ensamblado **Microsoft.Office.InfoPath.FormControl** se instalan junto con InfoPath en la carpeta C:\Program Files\Microsoft Office\Office15 o C:\Program Files (x86)\Microsoft Office\Office15 . 
  
El artículo de MSDN, que hospeda el entorno de edición de formularios de InfoPath 2007 en una aplicación de Windows Forms personalizada, se centra en el objeto **FormControl** y en cómo incorporarlo a su personalizado. Aplicaciones basadas en la red. Asociado a este artículo hay una aplicación personalizada que se puede descargar y que ofrece funciones de .NET para replicar el entorno de edición de formularios mediante el uso de **IOleCommandTargets** de COM.
  

