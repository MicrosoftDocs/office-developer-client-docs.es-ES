---
title: Integrar un formulario de InfoPath con una base de datos de Microsoft Access
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5ec9a9c0-b348-4a31-b377-e95db2f92455
description: Microsoft InfoPath admite el uso de una base de datos Microsoft Access 2010 como origen de datos principal de un formulario o como origen de datos secundario de un formulario o control. En este artículo se explica cómo usar una base de datos Access 2010 como origen de datos.
ms.openlocfilehash: 30aea15a5e9a8d19f64b3f089b71e859cff93e0e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815920"
---
# <a name="integrate-an-infopath-form-with-a-microsoft-access-database"></a>Integrar un formulario de InfoPath con una base de datos de Microsoft Access

Microsoft InfoPath admite el uso de una base de datos Microsoft Access 2010 como origen de datos principal de un formulario o como origen de datos secundario de un formulario o control. En este artículo se explica cómo usar una base de datos Access 2010 como origen de datos.
  
## <a name="using-a-microsoft-access-database-as-a-data-source"></a>Usar una base de datos de Microsoft Access como origen de datos

### <a name="setting-up-a-microsoft-access-database-as-a-forms-primary-data-source"></a>Configurar una base de datos de Microsoft Access como origen de datos principal de un formulario

Las conexiones de las bases de datos se establecen en InfoPath mediante el **Asistente para la conexión de datos**. Este asistente se abre seleccionando **Base de datos** en la sección **Plantillas de formulario avanzadas** de la pestaña **Nuevo** del Microsoft Office Backstage y, a continuación, haciendo clic en **Diseñar este formulario**.
  
Al hacer clic en **Seleccionar base de datos**, puede elegir un origen de datos existente o conectarse directamente con un archivo de bases de datos específico.
  
Una vez que selecciona la base de datos, el asistente le pedirá que seleccione una tabla de la base de datos para usarla como origen de datos del formulario. A medida que agregue tablas, se establecerán las relaciones entre ellas y el asistente mostrará las tablas y sus relaciones jerárquicas en la lista **Estructura del origen de datos**. Si activa la casilla de verificación **Mostrar las columnas de la tabla**, el asistente mostrará los nombres de los campos de cada tabla en la lista Estructura del origen de datos. Puede usar las casillas de verificación junto a cada nombre de campo para especificar si un campo está incluido en la instrucción SQL construida por el asistente. 
  
> [!NOTE]
> [!NOTA] Los datos principales de cada tabla siempre están seleccionados y no se pueden quitar. 
  
Cuando se han especificado las tablas, relaciones y campos mediante el **Asistente para la conexión de datos**, puede hacer clic en **Editar SQL** para ver la instrucción SQL que se usará para establecer el origen de datos del formulario. En el cuadro de diálogo **Editar SQL**, puede hacer clic en **Probar la instrucción SQL** para comprobar si InfoPath podrá crear el origen de datos por medio de la información proporcionada. También puede usar el cuadro de diálogo **Editar SQL** para modificar la instrucción SQL para crear consultas más complejas. 
  
> [!NOTE]
> [!NOTA] Las instrucciones SQL que usa InfoPath son consultas de forma de datos. Las consultas de forma de datos permiten la creación de relaciones jerárquicas entre dos o más entidades lógicas de una consulta. Es posible usar instrucciones JOIN de SQL, pero no se recomienda, ya que al hacerlo, se deshabilita el envío del formulario. Para obtener más información acerca de las consultas de forma de datos, vea la documentación en Microsoft Developer Network (MSDN). 
  
La última página del **Asistente para la conexión de datos** muestra información de resumen sobre el origen de datos, incluyendo el nombre y la ubicación del archivo de origen de datos, el nombre de la tabla primaria principal, la cantidad de tablas usadas y el estado del envío. El estado del envío le informará si la instrucción SQL generada permitirá el envío satisfactorio de datos al origen de datos. 
  
### <a name="setting-up-a-microsoft-access-database-as-a-secondary-data-source"></a>Configurar una base de datos de Microsoft Access como origen de datos secundario

Los orígenes de datos secundarios se pueden usar para proporcionar las entradas de un cuadro de lista o de un cuadro de lista desplegable, o se puede escribir código para agregar datos procedentes de un origen de datos secundario a un formulario. Para trabajar con orígenes de datos secundarios en un formulario, haga clic en **Conexiones de datos** en la pestaña **Datos** al diseñar un formulario. 
  
Cuando inicia el **Asistente para la conexión de datos**, se le pedirá que seleccione si desea recibir datos para usar en el formulario o enviar datos del formulario. Elija **Recibir datos** y, a continuación, haga clic en **Siguiente**. Para crear un origen de datos secundario desde una base de datos, seleccione **Base de datos (Microsoft SQL Server o Microsoft Office Access únicamente)**. En la siguiente página del asistente, haga clic en **Seleccionar base de datos** para elegir un origen de datos existente o para conectarse directamente con un archivo de base de datos específico. 
  
Una vez seleccionada una base de datos, el asistente le pide que seleccione una tabla o consulta de la base de datos para usarla como origen de datos del formulario. Para comenzar, debe seleccionar una tabla o consulta, pero podrá seleccionar tablas adicionales más tarde si desea incluirlas. Una vez seleccionada una tabla o consulta, el asistente le permite seleccionar los campos que desea usar en la lista **Estructura del origen de datos**. De forma predeterminada, todos los campos de la tabla están seleccionados, pero puede quitar los campos que no sean necesarios para el formulario. También puede controlar cómo se ordenan los registros devueltos por la tabla y si se permiten varios registros. Para hacerlo, haga clic en **Modificar tabla** y, a continuación, seleccione hasta tres criterios de ordenación en el cuadro de diálogo **Criterio de ordenación**. Cuando quede satisfecho, haga clic en **Finalizar**.
  
> [!NOTE]
> [!NOTA] Los datos principales de cada tabla siempre están seleccionados y no se pueden quitar. 
  
InfoPath también le permite recuperar datos de varias tablas o consultas al mismo tiempo. Cuando se recuperan datos de varias tablas o consultas, debe poder establecer una relación entre todas las tablas o consultas implicadas con la tabla o consulta original seleccionada en el **Asistente para la conexión de datos**. Por ejemplo, si estuviera recuperando datos de la tabla Clientes de la base de datos Neptuno, podría agregar la tabla Pedidos para recuperar datos de todos los pedidos de ese cliente y podría agregar la tabla Detalles del pedido para recuperar los detalles de cada pedido.
  
Para agregar una tabla adicional al origen de datos, seleccione la tabla a la que desea agregar una tabla secundaria de la lista **Estructura del origen de datos** y, a continuación, haga clic en **Agregar tabla**. Seleccione la tabla o consulta que desea agregar y, a continuación, haga clic en **Siguiente**. InfoPath le pedirá que seleccione la relación o relaciones que desea usar. Si los campos en las dos tablas tienen el mismo nombre, InfoPath agregará automáticamente esos campos como una relación, pero si no es así o si desea usar una relación personalizada, puede hacer clic en **Agregar relación** para especificar qué campos de la tabla primaria corresponden a campos de la tabla secundaria. También puede quitar relaciones existentes haciendo clic en **Quitar relación** en el cuadro de diálogo **Editar relación**. 
  
Cuando quede satisfecho con las relaciones, haga clic en **Finalizar**. Tal como se hizo con la tabla principal, podrá especificar qué campos debe devolver la tabla secundaria. Sin embargo, no podrá usar el botón **Modificar tabla** para editar el orden en que se devolverán los registros. 
  
Cuando haya especificado las tablas, relaciones y campos, puede hacer clic en **Editar SQL** para ver la instrucción de consulta SQL que se usará para establecer el origen de datos del formulario. En el cuadro de diálogo **Editar SQL**, puede hacer clic en **Probar la instrucción SQL** para comprobar si InfoPath podrá crear el origen de datos por medio de la información proporcionada. También puede usar el cuadro de diálogo **Editar SQL** para modificar la instrucción SQL para crear consultas más complejas. 
  
> [!NOTE]
> [!NOTA] Las instrucciones SQL que usa InfoPath son consultas de forma de datos. Las consultas de forma de datos permiten la creación de relaciones jerárquicas entre dos o más entidades lógicas de una consulta. Es posible usar instrucciones JOIN de SQL, pero no se recomienda, ya que al hacerlo, se deshabilita el envío del formulario. Para obtener más información acerca de las consultas de forma de datos, vea la documentación en Microsoft Developer Network (MSDN). 
  
## <a name="enabling-form-submission"></a>Habilitar el envío del formulario

Además de recibir datos desde una base de datos de Access, InfoPath puede enviar datos nuevos o cambiados de vuelta a la base de datos. Cuando se usa el comando **Enviar** de la pestaña **Inicio** o el Microsoft Office Backstage para enviar los cambios a la base de datos, InfoPath usa objetos de datos de ActiveX (ADO) para actualizar los registros de la base de datos. Se habilitará el envío del formulario cuando se cumplan todas las siguientes condiciones: 
  
- Debe haber una columna base para cada columna que se use en la consulta del formulario.
    
- La columna de una tabla no debe aparecer varias veces en toda la consulta.
    
- Una clave principal, restricción única o índice único deben estar disponibles para cada tabla de una cláusula SELECT usada en la consulta del formulario.
    
- Una tabla no se puede incluir varias veces en la consulta del formulario.
    
- Las relaciones entre las tablas primarias y secundarias deben incluir todas las columnas principales de la tabla primaria.
    
- Solo puede haber una tabla base para todas las columnas de una cláusula SELECT que se usa en la consulta del formulario.
    
Existen algunas circunstancias bajo las cuales InfoPath no puede enviar cambios del formulario a una base de datos. Por ejemplo, si crea un formulario que extrae datos de una consulta en lugar de una tabla o si personaliza la instrucción SQL usada por InfoPath para incluir una instrucción JOIN, InfoPath no podrá enviar los cambios. Otra circunstancia que impide que InfoPath envíe cambios se produce si se agregan al formulario tablas que tienen una relación de varios a uno con su tabla primaria. En situaciones en las que InfoPath no puede enviar cambios a la base de datos, el campo **Enviar estado** de la última página del **Asistente para la conexión de datos** mostrará la razón de la limitación. 
  

