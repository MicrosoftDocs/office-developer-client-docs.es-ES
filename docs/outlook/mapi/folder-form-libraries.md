---
title: Bibliotecas de formularios de carpetas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 62b7480e-b3eb-45fb-b74d-62f1dc918a53
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: ec12cf567dbbd8c1710f835a3c19369dd3626fd4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414287"
---
# <a name="folder-form-libraries"></a>Bibliotecas de formularios de carpetas

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
En algunos casos, es posible que desee asociar uno o más formularios a una carpeta específica. Por ejemplo, los empleados de la organización podrían tener una carpeta Informe de progreso en su almacén de mensajes personales para crear y almacenar informes de progreso. Dado que el informe de progreso es específico de la carpeta Informe de progreso de cada usuario, puede que no sea adecuado almacenar el formulario de informe de progreso en la biblioteca de formularios de todo el sistema. Sin embargo, se puede conservar una copia del formulario de informe de progreso en la tabla de contenido asociado de la carpeta Informe de progreso de cada usuario. Esto restringe al usuario el uso de formularios de informe de progreso fuera de la carpeta designada.
  
Conceptualmente, hay una biblioteca de formularios de carpeta para cada carpeta de un almacén de mensajes, incluso si no hay ningún servidor de formulario instalado en él. Las bibliotecas de formularios de carpetas se implementan como otras bibliotecas de formularios: se almacenan como tablas de contenido asociado en la parte alternativa de la carpeta. Dado que las bibliotecas de formularios de carpetas están contenidas en la carpeta, se copian junto con su carpeta principal en las operaciones de copia.
  
## <a name="see-also"></a>Consulte también



[Formularios MAPI](mapi-forms.md)

