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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281560"
---
# <a name="folder-form-libraries"></a>Bibliotecas de formularios de carpetas

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
En algunos casos, es posible que desee asociar uno o más formularios con una carpeta específica. Por ejemplo, los empleados de su organización podrían tener una carpeta de informe de progreso en su almacén personal de mensajes para crear y almacenar informes de progreso. Como el informe de progreso es específico de la carpeta de informes de progreso de cada usuario, puede que no sea adecuado almacenar el formulario de informe de progreso en la biblioteca de formularios de todo el sistema. Sin embargo, se puede conservar una copia del formulario del informe de progreso en la tabla de contenido asociado de la carpeta de informes de progreso de cada usuario. Esto impide que el usuario Use formularios de informe de progreso fuera de la carpeta designada.
  
Conceptualmente, hay una biblioteca de formularios de carpetas para cada carpeta de un almacén de mensajes, incluso si no hay servidores de formularios instalados en ella. Las bibliotecas de formularios de carpeta se implementan como otras bibliotecas de formularios, que se almacenan como tablas de contenido asociado en la parte alternativa de la carpeta. Como las bibliotecas de formularios de carpeta están contenidas en la carpeta, se copian junto con la carpeta principal en operaciones de copia.
  
## <a name="see-also"></a>Vea también



[Formularios MAPI](mapi-forms.md)

