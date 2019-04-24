---
title: Instalar el PIA de Outlook y hacer referencia a él
TOCTitle: Installing and referencing the Outlook PIA
ms:assetid: b1afd047-dcbb-480f-ba74-993d7d7114cb
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb646840(v=office.15)
ms:contentKeyID: 55119774
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 45584ae0a7050aa769368db518c9efcd5db9975a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336879"
---
# <a name="installing-and-referencing-the-outlook-pia"></a>Instalar el PIA de Outlook y hacer referencia a él

Debe tener instalado el ensamblado de interoperabilidad primario (PIA) de Outlook en la caché global de ensamblados (GAC) para poder incorporar información del PIA en un complemento administrado de Outlook. De forma predeterminada, el PIA se instala automáticamente al instalar Office en el equipo de desarrollo. No obstante, si necesita instalar el PIA por separado, vea [Configurar un equipo para desarrollar soluciones de Office](https://docs.microsoft.com/visualstudio/vsto/configuring-a-computer-to-develop-office-solutions?view=vs-2017).


> [!NOTE] 
> Debe ser administrador en el equipo de desarrollo para instalar los PIA de Office.

Después de la instalación, si usa Visual Studio para crear un proyecto administrado, puede agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0. Posteriormente, en el examinador de objetos, en el espacio de nombres **Microsoft.Office.Interop.Outlook**, puede ver las interfaces administradas en el PIA que tienen nombres correspondientes a los objetos en el modelo de objetos de Outlook.

## <a name="see-also"></a>Vea también

- [Cómo: ensamblados de interoperabilidad primarios de Office de instalación](https://docs.microsoft.com/visualstudio/vsto/how-to-install-office-primary-interop-assemblies?view=vs-2017)
- [Architecture of the Outlook PIA](architecture-of-the-outlook-pia.md) (Arquitectura del PIA de Outlook)

