---
title: Liberar objetos sistemáticamente
TOCTitle: Systematically releasing objects
ms:assetid: d4cd1d8e-aae6-483b-a4d8-1656171e838d
ms:mtpsurl: https://msdn.microsoft.com/library/Bb623945(v=office.15)
ms:contentKeyID: 55119785
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5d71ffbdbd10657832a319e1e669f38f311ad99f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319246"
---
# <a name="systematically-releasing-objects"></a>Liberar objetos sistemáticamente

En este tema se resumen las recomendaciones sobre el cierre de complementos para los programadores de complementos y administradores de TI que utilizan Outlook. Para obtener más información, vea [Cambios en el cierre de Outlook 2010](https://msdn.microsoft.com/library/ee720183\(v=office.15\)).

## <a name="add-in-shutdown-changes-in-outlook"></a>Cambios en el cierre de complementos de Outlook

Desde Outlook 2010, Outlook, de forma predeterminada, no indica a los complementos que se está cerrando. En concreto, Outlook ya no llama a los métodos **OnBeginShutdown(Array)** y **OnDisconnection (ext\_DisconnectMode, Array)** de la interfaz **IDTExtensibility2** durante el apagado rápido. De forma similar, un complemento de Outlook, escrito con las herramientas de desarrollo de Office en Visual Studio 2010 o una versión posterior, ya no llama al método ThisAddin\_Shutdown cuando se cierra Outlook. 

La razón para dejar de llamar a estos métodos es que aunque la mayoría de los complementos realizan tareas sencillas como publicar referencias, algunos complementos realizan llamadas de servicio Web u otras operaciones de ejecución prolongada de forma sincrónica durante estos eventos, lo que retrasa significativamente el cierre de Outlook. Como resultado de este cambio, Outlook funciona mejor durante el cierre que como lo hacía anteriormente.

## <a name="recommendations-for-add-in-shutdown-for-developers"></a>Recomendaciones sobre el cierre de complementos para programadores

Es importante que los programadores respeten las siguientes recomendaciones para el cierre de complementos con el fin de garantizar que los usuarios finales continúen beneficiándose de una experiencia de cierre de Outlook rápida y receptiva. 

- Los complementos deben continuar implementando los métodos OnBeginShutdown y OnDisconnection o ThisAddin\_Shutdown para liberar las referencias y la memoria asignada. Esto se debe a que existen escenarios en los que los administradores podrían volver al cierre lento a través de una directiva de grupo o el usuario podría desconectar manualmente el complemento a través del cuadro de diálogo **Complementos COM**.

- Los desarrolladores de complementos solo deben realizar tareas que requieran tener lugar durante el cierre.

- Los programadores de complementos deben evaluar el rendimiento de sus complementos en diversos escenarios y en diferentes configuraciones del Registro de Windows que controlan el cierre de Outlook y modificar, de forma activa, los complementos para que funcionen con Outlook.

## <a name="recommendations-for-add-in-shutdown-for-it-administrators"></a>Recomendaciones sobre el cierre de complementos para programadores de TI

Para los administradores de TI, si hay complementos que ya se han implementado en una empresa y no se puede actualizar para ser compatibles con el nuevo mecanismo de cierre de Outlook, los administradores de TI pueden recurrir a un par de opciones de configuración del Registro de Windows para volver al comportamiento de cierre lento.

### <a name="individual-add-in-setting"></a>Configuración de un complemento individual

Los administradores de TI pueden habilitar notificaciones de cierre para complementos individuales de Outlook como parte de la implementación del complemento. Aunque no puede hacerlo a través de una directiva de grupo, es útil si tiene requisitos de compatibilidad con versiones anteriores para complementos específicos.

Configure este valor para cada complemento mediante el registro de complementos en los subárboles del Registro HKCU o HKLM, agregando un valor adicional al registro del complemento. Escriba el texto siguiente como una sola línea:

`HKCU\Software\Microsoft\Office\Outlook\Add-ins\<ProgID>[RequireShutdownNotification]=dword:0x1`

Establecer este valor en 0x1 habilita el complemento para recibir callbacks bloqueadas durante el cierre de Outlook. Esto influye en el rendimiento del cierre de Outlook y se debe evaluar como parte de una implementación. Esta configuración solo debería usarse si un complemento tiene problemas de compatibilidad importantes con el nuevo mecanismo de cierre. Si se establece este valor en 0x0, se usa el comportamiento predeterminado de Outlook.

### <a name="global-setting"></a>Configuración global

Los administradores de TI pueden habilitar las notificaciones de cierre globalmente para todos los complementos mediante las directivas de grupo. Se recomienda para las organizaciones que tienen un gran número de soluciones internas o escritorios que necesitan implementar esta configuración para garantizar la compatibilidad durante una ejecución de Outlook.

Use esta opción para cambiar el mecanismo de cierre para que coincida con el usado en Outlook 2007. Puede implementar la configuración mediante directivas de grupo, ya sea por usuario o por equipo. Escriba lo siguiente en una sola línea:

`HKCU\Policies\Microsoft\Office\Outlook\15.0\Options\Shutdown[AddinFastShutdownBehavior]=dword:0x1`

Al establecer AddinFastShutdownBehavior en 0x1, se habilitan las notificaciones de cierre para todos los complementos. Si se establece el valor en 0x0, se usa el comportamiento predeterminado de Outlook.

