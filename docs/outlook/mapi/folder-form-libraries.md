---
title: Bibliotecas de formularios de carpeta
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 62b7480e-b3eb-45fb-b74d-62f1dc918a53
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: f5ce900fee3d40a46e66ac8f74f111db33d7522e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816830"
---
# <a name="folder-form-libraries"></a>Bibliotecas de formularios de carpeta

  
  
**Se aplica a**: Outlook 
  
En algunos casos, es posible que desee asociar uno o varios formularios a una carpeta específica. Por ejemplo, los empleados de su organización podrían tener una carpeta de informes de progreso en su almacén de mensajes personal para crear y almacenar los informes de progreso. Debido a que el informe de progreso es específico de informe de progreso de la carpeta de cada usuario, podría no ser apropiado almacenar el formulario de informe de progreso en la biblioteca de formulario todo el sistema. Sin embargo, se puede mantener una copia del formulario de informe de progreso en la tabla de contenido asociados de la carpeta de informes de progreso de cada usuario. Esto impide que el usuario mediante formularios de informe de progreso fuera de la carpeta designada.
  
Conceptualmente, hay una biblioteca de formularios de carpeta para todas las carpetas de un almacén de mensajes, incluso si no hay servidores de formulario están instaladas en ella. Las bibliotecas de formularios de carpeta se implementan como otras bibliotecas de formularios, se almacenan como tablas de contenido asociado en el elemento de la carpeta alternativa. Debido a que las bibliotecas de formularios de carpeta están contenidas en la carpeta, se copian junto con su carpeta primaria en las operaciones de copia.
  
## <a name="see-also"></a>Ver también



[Formularios MAPI](mapi-forms.md)

