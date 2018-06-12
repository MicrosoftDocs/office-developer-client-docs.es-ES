---
title: Ejemplo de proveedor de transporte
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ec6eb6c0-bfe3-4989-9071-89a14c0e7bdd
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 1d0538f02f852580c064560460bb8b2ba54a2f65
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820923"
---
# <a name="transport-provider-sample"></a><span data-ttu-id="1158d-103">Ejemplo de proveedor de transporte</span><span class="sxs-lookup"><span data-stu-id="1158d-103">Transport Provider Sample</span></span>

  
  
<span data-ttu-id="1158d-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1158d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1158d-105">Este ejemplo utiliza los archivos y directorios para transmitir y recibir mensajes.</span><span class="sxs-lookup"><span data-stu-id="1158d-105">This sample uses files and directories to transmit and receive messages.</span></span> <span data-ttu-id="1158d-106">Se implementa y se registra un preprocesador muy simple que anexa una línea de texto a cada mensaje saliente.</span><span class="sxs-lookup"><span data-stu-id="1158d-106">It implements and registers a very simple preprocessor that appends a line of text to each outbound message.</span></span> <span data-ttu-id="1158d-107">El ejemplo muestra cómo dividir el contenido de los mensajes entre el formato de encapsulación neutro de transporte (TNEF) y texto.</span><span class="sxs-lookup"><span data-stu-id="1158d-107">The sample illustrates how to split message content between Transport Neutral Encapsulation Format (TNEF) and text.</span></span> <span data-ttu-id="1158d-108">También es compatible con todas las opciones de configuración (hojas de propiedades, asistentes y configuración mediante programación) y las opciones de mensajes.</span><span class="sxs-lookup"><span data-stu-id="1158d-108">It also supports all configuration options (property sheets, wizards, and programmatic configuration) and message options.</span></span> <span data-ttu-id="1158d-109">No admite las interfaces de transporte remoto.</span><span class="sxs-lookup"><span data-stu-id="1158d-109">It does not support the remote transport interfaces.</span></span> 
  
<span data-ttu-id="1158d-110">Puede descargar este ejemplo de [Ejemplos de código de API de mensajería de Outlook (MAPI)](http://go.microsoft.com/fwlink/?LinkId=129740).</span><span class="sxs-lookup"><span data-stu-id="1158d-110">You can download this sample from [Outlook Messaging API (MAPI) Code Samples](http://go.microsoft.com/fwlink/?LinkId=129740).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1158d-111">Archivo ejecutable:</span><span class="sxs-lookup"><span data-stu-id="1158d-111">Executable:</span></span>  <br/> |<span data-ttu-id="1158d-112">mrxp32.dll</span><span class="sxs-lookup"><span data-stu-id="1158d-112">mrxp32.dll</span></span>  <br/> |
|<span data-ttu-id="1158d-113">Directorio de origen del código:</span><span class="sxs-lookup"><span data-stu-id="1158d-113">Source code directory:</span></span>  <br/> |<span data-ttu-id="1158d-114">SampleTransportProvider\MRXP</span><span class="sxs-lookup"><span data-stu-id="1158d-114">SampleTransportProvider\MRXP</span></span>  <br/> |
|<span data-ttu-id="1158d-115">Idioma:</span><span class="sxs-lookup"><span data-stu-id="1158d-115">Language:</span></span>  <br/> |<span data-ttu-id="1158d-116">C++</span><span class="sxs-lookup"><span data-stu-id="1158d-116">C++</span></span>  <br/> |
|<span data-ttu-id="1158d-117">Plataformas:</span><span class="sxs-lookup"><span data-stu-id="1158d-117">Platforms:</span></span>  <br/> |<span data-ttu-id="1158d-118">Visual Studio 2008 para compilar para Windows Vista, Windows Server 2008, Windows XP SP2 y Windows Server 2003 SP1</span><span class="sxs-lookup"><span data-stu-id="1158d-118">Visual Studio 2008 to compile for Windows Vista, Windows Server 2008, Windows XP SP2, and Windows Server 2003 SP1</span></span>  <br/> |
   
## <a name="supported-features"></a><span data-ttu-id="1158d-119">Características admitidas</span><span class="sxs-lookup"><span data-stu-id="1158d-119">Supported Features</span></span>

<span data-ttu-id="1158d-120">En este ejemplo es compatible con las siguientes características:</span><span class="sxs-lookup"><span data-stu-id="1158d-120">This sample supports the following features:</span></span>
  
- <span data-ttu-id="1158d-121">Características básicas, como enviar, recibir y para nuevos mensajes de sondeo.</span><span class="sxs-lookup"><span data-stu-id="1158d-121">Basic features such as sending, receiving, and polling for new messages.</span></span>
    
- <span data-ttu-id="1158d-122">Configuración interactiva y mediante programación.</span><span class="sxs-lookup"><span data-stu-id="1158d-122">Interactive and programmatic configuration.</span></span>
    
- <span data-ttu-id="1158d-123">La interfaz **IMAPIStatus** , excepto por el valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="1158d-123">The **IMAPIStatus** interface, except for property setting.</span></span> <span data-ttu-id="1158d-124">Para obtener más información, vea el [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) interfaz.</span><span class="sxs-lookup"><span data-stu-id="1158d-124">For more information, see the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> 
    
- <span data-ttu-id="1158d-125">Seguridad de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="1158d-125">Thread safety.</span></span>
    
- <span data-ttu-id="1158d-126">Registro de eventos en un archivo de texto.</span><span class="sxs-lookup"><span data-stu-id="1158d-126">Event logging to a text file.</span></span> <span data-ttu-id="1158d-127">El archivo se limita automáticamente a un tamaño especificado.</span><span class="sxs-lookup"><span data-stu-id="1158d-127">The file is automatically limited to a specified size.</span></span> <span data-ttu-id="1158d-128">Todas las sesiones de transporte usan el mismo archivo.</span><span class="sxs-lookup"><span data-stu-id="1158d-128">All transport sessions use the same file.</span></span>
    
## <a name="unsupported-features"></a><span data-ttu-id="1158d-129">Características no admitidas</span><span class="sxs-lookup"><span data-stu-id="1158d-129">Unsupported Features</span></span>

<span data-ttu-id="1158d-130">En este ejemplo no es compatible con detección asincrónica de los mensajes entrantes.</span><span class="sxs-lookup"><span data-stu-id="1158d-130">This sample does not support asynchronous detection of incoming messages.</span></span>
  
 <span data-ttu-id="1158d-131">**Para instalar al proveedor de transporte de ejemplo**</span><span class="sxs-lookup"><span data-stu-id="1158d-131">**To install the Sample Transport Provider**</span></span>
  
1. <span data-ttu-id="1158d-132">Para descargar el proveedor de transporte de ejemplo, consulte [descargar los ejemplos de MAPI de Outlook](downloading-the-outlook-mapi-samples.md).</span><span class="sxs-lookup"><span data-stu-id="1158d-132">To download the Sample Transport Provider, see [Downloading the Outlook MAPI Samples](downloading-the-outlook-mapi-samples.md).</span></span>
    
2. <span data-ttu-id="1158d-133">Busque la carpeta donde guardó los ejemplos de MAPI de Outlook.</span><span class="sxs-lookup"><span data-stu-id="1158d-133">Locate the folder where you saved the Outlook MAPI samples.</span></span> <span data-ttu-id="1158d-134">Haga clic en el **OutlookMAPISamples -\<número de versión\> ** zip carpeta y haga clic en **Extraer todos**.</span><span class="sxs-lookup"><span data-stu-id="1158d-134">Right-click the **OutlookMAPISamples-\<version number\>** zip folder and click **Extract All**.</span></span>
    
3. <span data-ttu-id="1158d-135">Haga clic en **Examinar**, seleccione la ubicación donde desea guardar el ejemplo y haga clic en **extraer**.</span><span class="sxs-lookup"><span data-stu-id="1158d-135">Click **Browse**, select the location where you want to save the sample, and click **Extract**.</span></span>
    
4. <span data-ttu-id="1158d-136">Ejecute Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="1158d-136">Run Visual Studio 2008.</span></span>
    
5. <span data-ttu-id="1158d-137">En Visual Studio 2008, haga clic en **archivo**, seleccione **Abrir**y, a continuación, haga clic en **Proyecto o solución**.</span><span class="sxs-lookup"><span data-stu-id="1158d-137">In Visual Studio 2008, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
6. <span data-ttu-id="1158d-138">Vaya a la ubicación donde guardó el ejemplo, haga clic en **mrxp32.vcproj**y, a continuación, haga clic en **Abrir**.</span><span class="sxs-lookup"><span data-stu-id="1158d-138">Browse to the location where you saved the sample, click **mrxp32.vcproj**, and then click **Open**.</span></span>
    
7. <span data-ttu-id="1158d-139">En el menú **Generar** , haga clic en **Administrador de configuración**.</span><span class="sxs-lookup"><span data-stu-id="1158d-139">On the **Build** menu, click **Configuration Manager**.</span></span>
    
8. <span data-ttu-id="1158d-140">En el cuadro de diálogo **Administrador de configuración** , vaya a la fila **mrxp32** y en la columna **configuración** , seleccione **versión**y, a continuación, haga clic en **Cerrar**.</span><span class="sxs-lookup"><span data-stu-id="1158d-140">In the **Configuration Manager** dialog box, go to the **mrxp32** row, and in the **Configuration** column select **Release**, and then click **Close**.</span></span>
    
9. <span data-ttu-id="1158d-141">On the **Build** menu, click **Build Solution**.</span><span class="sxs-lookup"><span data-stu-id="1158d-141">On the **Build** menu, click **Build Solution**.</span></span>
    
10. <span data-ttu-id="1158d-142">En el cuadro de diálogo **Guardar archivo como** , haga clic en **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="1158d-142">In the **Save File As** dialog box, click **Save**.</span></span>
    
11. <span data-ttu-id="1158d-143">En la carpeta donde guardó el ejemplo, haga clic en el archivo por lotes de instalación y haga clic en **Ejecutar como administrador**.</span><span class="sxs-lookup"><span data-stu-id="1158d-143">In the folder where you saved the sample, right-click the installation batch file and click **Run as administrator**.</span></span>
    
12. <span data-ttu-id="1158d-144">En el cuadro de diálogo **Control de cuentas de usuario** , haga clic en **continuar**.</span><span class="sxs-lookup"><span data-stu-id="1158d-144">In the **User Account Control** dialog box, click **Continue**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="1158d-145">**Install.bat** copia el archivo .dll en la carpeta de instalación de Microsoft Office de forma predeterminada, C:\Program Files\Microsoft Office\Office12\.</span><span class="sxs-lookup"><span data-stu-id="1158d-145">**install.bat** copies the .dll to the default Microsoft Office installation folder, C:\Program Files\Microsoft Office\Office12\.</span></span> <span data-ttu-id="1158d-146">Si ha instalado productos de Office en una ubicación diferente, haga clic en **install.bat** y haga clic en **Editar**.</span><span class="sxs-lookup"><span data-stu-id="1158d-146">If you have installed Office products in a different location, right-click **install.bat** and click **Edit**.</span></span> <span data-ttu-id="1158d-147">El archivo se abre en el Bloc de notas.</span><span class="sxs-lookup"><span data-stu-id="1158d-147">The file opens in Notepad.</span></span> <span data-ttu-id="1158d-148">Reemplace la ruta de instalación predeterminada con la ruta de instalación utilizada en el equipo.</span><span class="sxs-lookup"><span data-stu-id="1158d-148">Replace the default installation path with the installation path used on your computer.</span></span> 
  
 <span data-ttu-id="1158d-149">**Para configurar el proveedor de transporte en Outlook**</span><span class="sxs-lookup"><span data-stu-id="1158d-149">**To set up the Transport Provider in Outlook**</span></span>
  
1. <span data-ttu-id="1158d-150">En el menú **Herramientas** de Outlook, haga clic en **Configuración de la cuenta**.</span><span class="sxs-lookup"><span data-stu-id="1158d-150">On the **Tools** menu of Outlook, click **Account Settings**.</span></span>
    
2. <span data-ttu-id="1158d-151">En el cuadro de diálogo **Configuración de la cuenta** , en la ficha **correo electrónico** , haga clic en **nuevo**.</span><span class="sxs-lookup"><span data-stu-id="1158d-151">In the **Account Settings** dialog box, on the **Email** tab, click **New**.</span></span>
    
3. <span data-ttu-id="1158d-152">En **Elegir servicio de correo electrónico** haga clic en **otros**, seleccione **MRXP ejemplo de transporte**y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="1158d-152">Under **Choose Email Service** click **Other**, select **MRXP Sample Transport**, and then click **Next**.</span></span>
    
4. <span data-ttu-id="1158d-153">En el cuadro de diálogo **Configuración de transporte MRXP** escriba un **Nombre de usuario para mostrar**.</span><span class="sxs-lookup"><span data-stu-id="1158d-153">In the **MRXP Transport Configuration** dialog box type a **User Display Name**.</span></span>
    
5. <span data-ttu-id="1158d-154">En la **ruta de acceso a la Bandeja de entrada (recurso compartido UNC)** , escriba una ruta de acceso de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="1158d-154">Under **Path to Inbox (UNC Share)** enter a folder path.</span></span> <span data-ttu-id="1158d-155">Esto también puede ser una ruta de acceso a una carpeta local.</span><span class="sxs-lookup"><span data-stu-id="1158d-155">This can also be a path to a local folder.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="1158d-156">Esta ruta de acceso debe existir.</span><span class="sxs-lookup"><span data-stu-id="1158d-156">This path must exist.</span></span> 
  
6. <span data-ttu-id="1158d-157">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="1158d-157">Click **OK**.</span></span>
    
7. <span data-ttu-id="1158d-158">En el cuadro de diálogo **Agregar una cuenta de correo electrónico** , haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="1158d-158">In the **Add Email Account** dialog box click **OK**.</span></span> <span data-ttu-id="1158d-159">Haga clic en **Finalizar** y, a continuación, haga clic en **Cerrar**.</span><span class="sxs-lookup"><span data-stu-id="1158d-159">Click **Finish** and then click **Close**.</span></span>
    
8. <span data-ttu-id="1158d-160">Para empezar a usar la cuenta de MRXP, salga y reinicie Outlook.</span><span class="sxs-lookup"><span data-stu-id="1158d-160">To start using the MRXP account, exit and restart Outlook.</span></span>
    
 <span data-ttu-id="1158d-161">**Para usar el ejemplo de proveedor de transporte para enviar un mensaje en Outlook**</span><span class="sxs-lookup"><span data-stu-id="1158d-161">**To use the Transport Provider Sample to send a message in Outlook**</span></span>
  
1. <span data-ttu-id="1158d-162">En el menú **archivo** , haga clic en **nuevo**y, a continuación, haga clic en **El mensaje de correo**.</span><span class="sxs-lookup"><span data-stu-id="1158d-162">On the **File** menu, click **New**, and then click **Mail Message**.</span></span>
    
2. <span data-ttu-id="1158d-163">En **el cuadro** escriba el nombre del destinatario con el formato **[MRXP:\<dirección\>]**.</span><span class="sxs-lookup"><span data-stu-id="1158d-163">In the **To** box type the name of the recipient using the format **[MRXP:\<ADDRESS\>]**.</span></span> <span data-ttu-id="1158d-164">La dirección es el recurso compartido UNC o una ruta de acceso de carpeta local a la Bandeja de entrada del destinatario.</span><span class="sxs-lookup"><span data-stu-id="1158d-164">The address is the UNC share or local folder path to the recipient's inbox.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="1158d-165">Si hay dos puntos o barras diagonales inversas en la dirección, debe insertar una barra diagonal inversa antes de cada carácter de dos puntos o una barra diagonal inversa.</span><span class="sxs-lookup"><span data-stu-id="1158d-165">If there are colons or backslashes in the address, you must insert a backslash before each colon or backslash.</span></span> <span data-ttu-id="1158d-166">Por ejemplo, para enviar correo a [MRXP:C:\Mail\myDir] debe que escribir `[MRXP:C\:\\Mail\\myDir]`.</span><span class="sxs-lookup"><span data-stu-id="1158d-166">For example, to send mail to [MRXP:C:\Mail\myDir] you must type  `[MRXP:C\:\\Mail\\myDir]`.</span></span> 
  
    > [!IMPORTANT]
    > <span data-ttu-id="1158d-167">Debe existir la dirección del destinatario.</span><span class="sxs-lookup"><span data-stu-id="1158d-167">The recipient address must exist.</span></span> 
  
3. <span data-ttu-id="1158d-168">Haga clic en **cuenta** y, a continuación, haga clic en **Transporte de ejemplo MRXP**.</span><span class="sxs-lookup"><span data-stu-id="1158d-168">Click **Account** and then click **MRXP Sample Transport**.</span></span>
    
4. <span data-ttu-id="1158d-169">Escriba el mensaje y haga clic en **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="1158d-169">Type your message and click **Send**.</span></span> <span data-ttu-id="1158d-170">El mensaje se envía con el proveedor de transporte MRXP.</span><span class="sxs-lookup"><span data-stu-id="1158d-170">The message is sent using the MRXP transport provider.</span></span>
    
 <span data-ttu-id="1158d-171">**Para usar el ejemplo de proveedor de transporte para recibir un mensaje en Outlook**</span><span class="sxs-lookup"><span data-stu-id="1158d-171">**To use the Transport Provider Sample to receive a message in Outlook**</span></span>
  
1. <span data-ttu-id="1158d-172">En el menú **archivo** , haga clic en **nuevo**y, a continuación, haga clic en **El mensaje de correo**.</span><span class="sxs-lookup"><span data-stu-id="1158d-172">On the **File** menu, click **New**, and then click **Mail Message**.</span></span>
    
2. <span data-ttu-id="1158d-173">Escriba el mensaje.</span><span class="sxs-lookup"><span data-stu-id="1158d-173">Type your message.</span></span>
    
3. <span data-ttu-id="1158d-174">Haga clic en el **Botón de Microsoft Office**, haga clic en **Guardar como**y, a continuación, haga clic en **Guardar como** para guardar el archivo en la carpeta Bandeja de entrada especificados durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="1158d-174">Click the **Microsoft Office Button**, click **Save As**, and then click **Save As** to save the file to the inbox folder you specified during setup.</span></span> 
    
4. <span data-ttu-id="1158d-175">En el cuadro de diálogo **Guardar como** , busque el recurso compartido UNC o una carpeta local que ha configurado como la Bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="1158d-175">In the **Save As** dialog box, browse to the UNC share or local folder that you set as your inbox.</span></span> 
    
5. <span data-ttu-id="1158d-176">En la lista **Guardar como tipo** desplegable, haga clic en **Formato de mensaje de Outlook**.</span><span class="sxs-lookup"><span data-stu-id="1158d-176">In the **Save as type** drop down, click **Outlook Message Format**.</span></span>
    
6. <span data-ttu-id="1158d-177">Escriba un nombre para el archivo y haga clic en **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="1158d-177">Type a name for the file and click **Save**.</span></span>
    
7. <span data-ttu-id="1158d-178">El archivo se guarda en la carpeta compartida.</span><span class="sxs-lookup"><span data-stu-id="1158d-178">The file is saved to the shared folder.</span></span> <span data-ttu-id="1158d-179">El proveedor de transporte MRXP entrega el mensaje a la Bandeja de entrada en Outlook.</span><span class="sxs-lookup"><span data-stu-id="1158d-179">The MRXP transport provider delivers the message to your Inbox in Outlook.</span></span>
    

