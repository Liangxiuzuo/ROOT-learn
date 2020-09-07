{
  h1 = new TH1F("h1","h1",100,-5,5);
  h2 = new TH1F("h2","h2",100,-5,5);
  h3 = new TH1F("h3","h3",100,-5,5);
  
  h1->FillRandom("gaus");
  h2->FillRandom("gaus");
  h3->FillRandom("gaus");
  
  h1->Draw();
  h2->Draw("sames"); // sames != same
  h3->Draw("sames");
  gPad->Update();
  
  TPaveStats *st1 = (TPaveStats*)h1->FindObject("stats");
  Double_t defaulth = st1->GetY2NDC() - st1->GetY1NDC();
  Double_t gaph = 0.02;
  
  TPaveStats *st2 = (TPaveStats*)h2->FindObject("stats");
  st2->SetOptStat(11);
  st2->SetY1NDC(st1->GetY1NDC() - 0.5*defaulth);
  st2->SetY2NDC(st1->GetY1NDC() - gaph);
  
  TPaveStats *st3 = (TPaveStats*)h3->FindObject("stats");
  st3->SetY1NDC(st2->GetY1NDC() - defaulth);
  st3->SetY2NDC(st2->GetY1NDC() - gaph);
  
  gPad->Modified();
  gPad->Update();
}
